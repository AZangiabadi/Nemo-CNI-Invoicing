On Mac:

cd /Users/folderName/containing-files
python3 -m venv .venv
source .venv/bin/activate
pip3 install -r requirements.txt
uvicorn app:app --host 127.0.0.1 --port 8000


cloudflared tunnel --url http://127.0.0.1:8000

On Windows CMD:
python -m venv .venv
.\.venv\Scripts\activate.bat
python -m pip install -r requirements.txt
python -m uvicorn app:app --host 0.0.0.0 --port 8000


To publish online:

cloudflared tunnel --url http://127.0.0.1:8000
or
ngrok http 8000
