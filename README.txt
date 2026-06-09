═══════════════════════════════════════
 اتمتها — مدرب المبيعات  |  SETUP GUIDE
═══════════════════════════════════════

REQUIREMENTS
────────────
• macOS / Windows / Linux
• Google Chrome (required for voice recognition)
• Ollama installed on your machine

STEP 1 — Install Ollama
───────────────────────
Go to: https://ollama.ai
Download and install for your OS.

STEP 2 — Enable CORS (required for the app to talk to Ollama)
─────────────────────────────────────────────────────────────
On Mac, run in Terminal:
  launchctl setenv OLLAMA_ORIGINS "*"

Then restart Ollama from the menu bar icon (quit + reopen).

Or set it permanently:
  echo 'OLLAMA_ORIGINS="*"' >> ~/.zshrc && source ~/.zshrc

STEP 3 — Pull the AI model
───────────────────────────
Open Terminal and run:
  ollama pull llama3.1

This downloads ~4GB. Wait for it to complete.

STEP 4 — Start Ollama
──────────────────────
Ollama should start automatically. If not:
  ollama serve

STEP 5 — Open the App
──────────────────────
Drag index.html into Google Chrome.
Or double-click index.html (may need to right-click → Open With → Chrome).

USING THE APP
─────────────
1. Select difficulty (سهل / متوسط / صعب)
2. Wait for green dot confirming Ollama is ready
3. Click "ابدأ الجلسة" — the prospect will open
4. Press SPACE or click 🎙️ to start speaking
5. Press SPACE again to stop recording
6. Press ENTER or click "إرسال" to send your reply
7. The coach panel on the right shows your score after each turn
8. Click "انهاء الجلسة" when done for a full debrief

KEYBOARD SHORTCUTS
──────────────────
Space   = toggle mic on/off
Enter   = send your message

TIPS
────
• Use Chrome — Firefox/Safari don't support voice recognition well
• Speak clearly in any Arabic dialect or English — the mic understands both
• The prospect speaks Saudi Najdi Arabic with browser TTS (quality varies by OS)
• On Mac, go to System Settings → Accessibility → Spoken Content → add Arabic voice
  for better TTS quality
• Hard mode is very realistic — the prospect will push back hard

TROUBLESHOOTING
───────────────
"Ollama مو شغال"
→ Make sure Ollama is running: open Terminal → type: ollama serve
→ Make sure CORS is enabled (Step 2)

"الموديل غير موجود"
→ Run: ollama pull llama3.1

Mic not working
→ Chrome will ask for microphone permission — click Allow
→ Must be on file:// or https:// (file:// works fine)

Prospect replies in English
→ This happens with some models. llama3.1 works best for Arabic.
   You can also try: qwen2.5 (good Arabic support)
