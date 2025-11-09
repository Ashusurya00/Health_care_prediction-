<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Healthcare Prediction System — README</title>
  <style>
    :root{
      --bg:#0f1724;
      --card:#0b1220;
      --accent:#06b6d4;
      --muted:#9aa5b1;
      --text:#e6eef3;
      --glass: rgba(255,255,255,0.03);
      --code-bg:#0b1220;
      --pill-bg: rgba(255,255,255,0.04);
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      background: linear-gradient(180deg,#071022 0%, #071831 100%);
      color:var(--text);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      padding:32px;
      line-height:1.6;
    }
    .container{
      max-width:980px;
      margin:0 auto;
    }
    header{
      display:flex;
      gap:16px;
      align-items:center;
      margin-bottom:18px;
    }
    .logo{
      width:72px;
      height:72px;
      border-radius:12px;
      background:linear-gradient(135deg,var(--accent),#7c3aed);
      display:flex;
      align-items:center;
      justify-content:center;
      font-weight:700;
      font-size:20px;
      color:#02121a;
      box-shadow: 0 6px 20px rgba(3,7,18,0.6), inset 0 -6px 18px rgba(255,255,255,0.02);
    }
    h1{margin:0;font-size:22px}
    p.lead{color:var(--muted);margin-top:6px}
    .badges{display:flex;gap:8px;flex-wrap:wrap;margin-top:12px}
    .badge{background:var(--pill-bg);color:var(--text);padding:6px 10px;border-radius:999px;font-size:13px}
    main{
      margin-top:22px;
    }
    .card{
      background:var(--card);
      border-radius:12px;
      padding:20px;
      margin-bottom:18px;
      box-shadow: 0 6px 30px rgba(2,6,12,0.6);
      border:1px solid rgba(255,255,255,0.03);
    }
    h2{margin:0 0 8px 0;font-size:18px}
    pre{background:var(--code-bg);padding:14px;border-radius:8px;overflow:auto;border:1px solid rgba(255,255,255,0.02);font-family:ui-monospace, SFMono-Regular, Menlo, Monaco, "Roboto Mono", "Courier New", monospace;color:#bfeaf4}
    code{background:rgba(255,255,255,0.02);padding:2px 6px;border-radius:6px}
    .columns{display:grid;grid-template-columns:1fr 320px;gap:18px}
    .sidebar .card{position:sticky;top:32px}
    ul{padding-left:18px}
    .screenshot-grid{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:12px}
    img.screenshot{width:100%;height:180px;object-fit:cover;border-radius:8px;border:1px solid rgba(255,255,255,0.03)}
    .footer{color:var(--muted);font-size:13px;margin-top:12px}
    .cmd{display:block;background:var(--pill-bg);padding:10px;border-radius:8px;font-family:ui-monospace,monospace;margin:8px 0}
    .pill{display:inline-block;background:var(--pill-bg);padding:6px 10px;border-radius:999px;font-size:13px;margin-right:8px}
    table{width:100%;border-collapse:collapse;margin-top:8px}
    table th, table td{border-bottom:1px dashed rgba(255,255,255,0.03);padding:8px;text-align:left;font-size:14px}
    .muted{color:var(--muted)}
    .link{color:var(--accent);text-decoration:none}
    @media (max-width:900px){
      .columns{grid-template-columns:1fr}
      header{flex-direction:column;align-items:flex-start;gap:8px}
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="logo">HS</div>
      <div>
        <h1>Healthcare Prediction System — Deep Learning Project</h1>
        <p class="lead">AI-powered predictive system for patient risk assessment — built with TensorFlow, Keras, and Streamlit.</p>
        <div class="badges">
          <span class="badge">Python</span>
          <span class="badge">TensorFlow</span>
          <span class="badge">Keras</span>
          <span class="badge">Streamlit</span>
          <span class="badge">ML/Healthcare</span>
        </div>
      </div>
    </header>

    <main>
      <div class="columns">
        <section>
          <div class="card">
            <h2>Overview</h2>
            <p>
              This project is a Healthcare Prediction System that uses a deep neural network to predict health risk (e.g., disease likelihood) using clinical and lifestyle features.
              The app includes data preprocessing, model training, evaluation, and a Streamlit UI for real-time predictions.
            </p>
            <p class="muted">Model file: <code>health_model.h5</code> • Label mapping included • Streamlit UI: <code>app.py</code></p>
          </div>

          <div class="card">
            <h2>Features</h2>
            <ul>
              <li>Deep Neural Network (Keras/TensorFlow) for health risk prediction</li>
              <li>Data preprocessing: imputation, encoding, scaling</li>
              <li>Model evaluation: accuracy, confusion matrix, classification report</li>
              <li>Streamlit web app for predictions and visualization</li>
              <li>Model saved as <code>health_model.h5</code> for deployment</li>
            </ul>
          </div>

          <div class="card">
            <h2>Architecture</h2>
            <p class="muted">A compact, performant MLP used for binary risk prediction:</p>
            <pre><code>Input → Dense(64, ReLU) → Dense(32, ReLU) → Dense(16, ReLU) → Output(Sigmoid)</code></pre>
            <p class="muted">Loss: Binary Crossentropy • Optimizer: Adam • Regularization: Dropout & EarlyStopping</p>
          </div>

          <div class="card">
            <h2>Dataset</h2>
            <p>
              Replace the placeholder with your dataset (CSV). Typical columns:
              <code>age, bmi, blood_pressure, glucose, insulin, physical_activity, smoking, alcohol, outcome</code>.
            </p>
            <p class="muted">Example source: UCI / public health datasets. Use a train/validation split of 80/20.</p>
          </div>

          <div class="card">
            <h2>Installation</h2>
            <p>Run these commands to set up and run the app locally:</p>
            <pre><code># Clone
git clone https://github.com/<your-username>/healthcare-prediction-app.git
cd healthcare-prediction-app

# Create venv (Windows)
python -m venv venv
venv\Scripts\activate

# Install
pip install -r requirements.txt

# Run Streamlit app
streamlit run app.py
</code></pre>
            <p class="muted">Open <code>http://localhost:8501</code> after running.</p>
          </div>

          <div class="card">
            <h2>Usage</h2>
            <ol>
              <li>Open the Streamlit UI.</li>
              <li>Enter patient details or upload a CSV of patient data.</li>
              <li>Click <strong>Predict</strong> to see risk probability and classification (High/Low).</li>
              <li>View visualizations (ROC, confusion matrix) in the Evaluation tab.</li>
            </ol>
          </div>

          <div class="card">
            <h2>Results</h2>
            <p><strong>Validation Accuracy:</strong> 95% (example)</p>
            <table>
              <thead>
                <tr><th>Metric</th><th>Value</th></tr>
              </thead>
              <tbody>
                <tr><td>Accuracy</td><td>95%</td></tr>
                <tr><td>Precision</td><td>94%</td></tr>
                <tr><td>Recall</td><td>93%</td></tr>
                <tr><td>F1-score</td><td>93.5%</td></tr>
              </tbody>
            </table>
          </div>

          <div class="card">
            <h2>Screenshots</h2>
            <div class="screenshot-grid">
              <img class="screenshot" src="screenshots/home_ui.png" alt="Home UI (replace path)">
              <img class="screenshot" src="screenshots/prediction_result.png" alt="Prediction (replace path)">
            </div>
            <p class="muted" style="margin-top:10px">Replace screenshots/home_ui.png and prediction_result.png with real images.</p>
          </div>

          <div class="card">
            <h2>Code Snippets</h2>
            <p class="muted">Model training example:</p>
            <pre><code>from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense, Dropout

model = Sequential([
  Dense(64, activation='relu', input_shape=(n_features,)),
  Dropout(0.3),
  Dense(32, activation='relu'),
  Dense(16, activation='relu'),
  Dense(1, activation='sigmoid')
])

model.compile(optimizer='adam', loss='binary_crossentropy', metrics=['accuracy'])
model.fit(X_train, y_train, validation_data=(X_val,y_val), epochs=30, callbacks=[early_stop])</code></pre>
          </div>

          <div class="card">
            <h2>Future Enhancements</h2>
            <ul>
              <li>Explainability with SHAP or LIME</li>
              <li>Multi-disease risk prediction (heart disease, diabetes)</li>
              <li>Model deployment with REST API for hospital integration</li>
              <li>Real-time monitoring using IoT health sensors</li>
            </ul>
          </div>
        </section>

        <aside class="sidebar">
          <div class="card">
            <h2>Quick Links</h2>
            <p><a class="link" href="https://github.com/<your-username>/healthcare-prediction-app" target="_blank">GitHub Repo</a></p>
            <p><a class="link" href="https://streamlit.io" target="_blank">Streamlit</a> • <a class="link" href="https://www.tensorflow.org" target="_blank">TensorFlow</a></p>
            <div style="margin-top:10px">
              <span class="pill">Model: health_model.h5</span>
              <span class="pill">App: app.py</span>
            </div>
          </div>

          <div class="card">
            <h2>Deploy</h2>
            <p class="muted">Quick deploy options:</p>
            <ul>
              <li>Streamlit Cloud</li>
              <li>Render</li>
              <li>AWS EC2 with a simple nginx reverse-proxy</li>
            </ul>
            <p class="muted">For production, wrap the model with a Flask/FastAPI endpoint and secure it behind HTTPS.</p>
          </div>

          <div class="card">
            <h2>Contacts</h2>
            <p><strong>Ashutosh Suryawanshi</strong></p>
            <p class="muted">Email: <code>your-email@example.com</code></p>
            <p class="muted">LinkedIn: <a class="link" href="https://www.linkedin.com/in/your-linkedin" target="_blank">your-linkedin</a></p>
          </div>

          <div class="card">
            <h2>License</h2>
            <p class="muted">MIT License — feel free to reuse, adapt, and share.</p>
          </div>
        </aside>
      </div>

      <div class="footer">
        <p>⭐ If you found this useful, star the repo and share it! • Generated README HTML by ChatGPT.</p>
      </div>
    </main>
  </div>
</body>
</html>
