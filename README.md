git config --global user.name "AI_Agent_Zihad"
git config --global user.email "zihadsk44@gmail.com"
cd linera-protocol && git checkout -b feature/zihad
touch note.md && echo "Linera rocks!" > note.md
git add note.md
git commit -m "Add a friendly note: Linera rocks!"
git push origin feature/zihad# 1. Configure Git
git config --global user.name "zihad"
git config --global user.email "zihadsk44@gmail.com"

# 2. Go to your project folder
cd /path/to/your/project

# 3. Stage changes
git add .

# 4. Commit with a custom message
git commit -m "Hi from zihad"

# 5. Push to GitHub
git push origin main