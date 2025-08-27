**Credits**: Nethan Mikil Kuruppu https://github.com/atomikk65535

Also check out https://github.com/saatvik-agrawal/project-vitruvius

## How to use this quickly?

Check out https://huggingface.co/spaces/atomikk/PID

## 🚀 How to build this for yourself?

1. Clone the repository or open it in a GitHub Codespace.
2. Open the root folder in a terminal.
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Set up your environment variables (see Environment Variables section below).
5. Run:
   ```bash
   streamlit run app.py
   ```

## 🌐 Deployment

### Deploy to Streamlit Cloud

1. Push your code to GitHub
2. Visit [share.streamlit.io](https://share.streamlit.io)
3. Connect your GitHub repository
4. Add your `GOOGLE_API_KEY` in the Streamlit Cloud secrets management
5. Deploy!

### Environment Variables

Create a `.env` file in the root directory with:
```
GOOGLE_API_KEY=your_google_gemini_api_key_here
```

For Streamlit Cloud deployment, add this as a secret in your app settings.

---

## 📦 Requirements

Install these Python packages and libraries before running the app:

- `pyyaml` – for reading `.yaml` config files  
  ```bash
  pip install pyyaml
  ```

- `python-dotenv` – for loading environment variables from `.env`  
  ```bash
  pip install python-dotenv
  ```

- `streamlit` – for running the web app  
  ```bash
  pip install streamlit
  ```

Install all at once:
```bash
pip install pyyaml python-dotenv streamlit
```

---

## 📂 File Structure

```
project-root/
├── app.py
├── config.yaml
├── .env
├── README.md
```

---

## ℹ️ Notes

- `.env`: use `KEY=VALUE` format
- `.yaml`: follow standard YAML syntax
