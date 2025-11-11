

---

````md
Install Termux
https://play.google.com/store/apps/details?id=com.termux
then install python in it using
```sudo apt update
sudo apt install python3 -y
```
## 🐍 Running MSMC on Termux (Android)

Although MSMC was originally made for Windows, this modified version works on **Termux** for Android.

### ✅ Requirements
Make sure you have the following installed in Termux:
```bash
pkg update && pkg upgrade -y
pkg install git python -y
pip install --upgrade pip
````

### 🧩 Installation

```bash
git clone https://github.com/opbachhashiny/Msmc-termux/
cd Msmc-termux
pip install -r requirements.txt
```

### 📂 Preparing Files
**MUST DO ```nano config.ini``` and turn proxyless bancheck to false
Before running MSMC, make sure you create these files in the same folder as `MSMC.py`:

```
combos.txt      → list of email:password combos
proxies.txt     → list of proxies (ip:port or user:pass@ip:port)[optional can use proxyless]
```

Example:

```
combos.txt:
email1@gmail.com:password1
email2@hotmail.com:password2

proxies.txt:
103.172.70.27:8080
user:pass@8.9.10.11:1080
```

### ▶️ Running MSMC

Run it directly using:

```bash
python -m venv env
source env/bin/activate
python MSMC.py
```

* MSMC will automatically load `combos.txt` and `proxies.txt` from the same folder.
* No file picker or GUI dialogs are used (Termux compatible).
* You can use `Ctrl + C` to stop at any time.

### ⚙️ Notes

* Performance depends on your device and proxy quality.
* If you see SSL errors, try reinstalling dependencies:

  ```bash
  pip install requests urllib3 colorama
  ```
* Results are saved in the `results/` folder.
 you can do nano results/hits.txt to see hits
