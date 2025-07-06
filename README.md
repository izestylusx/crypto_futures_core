# 🎯 Panduan Lengkap Crypto Futures Core System

## 📋 Pengenalan

Selamat datang di **Crypto Futures Core System**! Ini adalah sistem AI agent canggih untuk trading crypto futures yang bekerja langsung di VS Code menggunakan GitHub Copilot. Sistem ini dirancang khusus untuk membantu trader dari pemula hingga profesional dalam menganalisis pasar, mengelola risiko, dan melakukan trading dengan lebih efektif.

### 🌟 Fitur Utama
- **AI Trading Agents** - Berbagai agent khusus untuk analisis pasar, manajemen risiko, dan eksekusi trading
- **Real-time Market Data** - Koneksi langsung dengan Binance Futures API
- **Risk Management** - Sistem manajemen risiko otomatis yang dapat disesuaikan
- **Technical Analysis** - Indikator teknikal lengkap dengan konfigurasi yang fleksibel
- **Workflow Automation** - Otomatisasi proses trading dari analisis hingga eksekusi

---

## 📖 Daftar Isi

### 🚀 Quick Start
- [1. Persyaratan & Persiapan](#-persyaratan--persiapan)
- [2. Instalasi Prerequisites](#-instalasi-prerequisites-windows)
- [3. Instalasi Premium Binance MCP Server](#-instalasi-premium-binance-mcp-server)
- [4. Cara Menggunakan Sistem](#-cara-menggunakan-sistem)
- [5. Mulai Trading Pertama Anda](#-mulai-trading-pertama-anda)

### 📚 Panduan Lengkap
- **[1. 🛠️ Persyaratan & Persiapan](#-persyaratan--persiapan)**
  - [Yang Anda Butuhkan](#yang-anda-butuhkan)
  - [Download & Setup Folder](#-download--setup-folder)

- **[2. 🔧 Instalasi Prerequisites (Windows)](#-instalasi-prerequisites-windows)**
  - [Install Python](#1-install-python-untuk-premium-binance-mcp)
  - [Install Node.js](#2-install-nodejs-untuk-sequential-thinking)
  - [Verifikasi Instalasi](#3-verifikasi-instalasi)
  - [Troubleshooting Prerequisites](#-troubleshooting-prerequisites)

- **[3. 🚀 Instalasi Premium Binance MCP Server](#-instalasi-premium-binance-mcp-server)**
  - [Step 1: Install Package Python](#step-1-install-package-python)
  - [Step 2: Konfigurasi Settings.json](#step-2-konfigurasi-settingsjson-vs-code)
  - [Step 3: Ganti API Keys](#step-3-ganti-api-keys)
  - [Step 4: Restart MCP Server](#step-4-restart-mcp-server)

- **[4. 🎮 Cara Menggunakan Sistem](#-cara-menggunakan-sistem)**
  - [Mulai dengan CFT Orchestrator](#1-mulai-dengan-cft-orchestrator)
  - [Command Dasar Sistem](#2-command-dasar-sistem)
  - [Contoh Penggunaan Praktis](#3-contoh-penggunaan-praktis)

- **[5. ⚙️ Kustomisasi Sistem](#-kustomisasi-sistem)**
  - [Mengatur Risk Profile](#1-mengatur-risk-profile)
  - [Mengatur Technical Indicators](#2-mengatur-technical-indicators)
  - [Membuat Strategy Custom](#3-membuat-strategy-custom)

- **[6. 🔥 Tips & Trik Penggunaan](#-tips--trik-penggunaan)**
  - [Best Practices](#-best-practices)
  - [Workflow yang Direkomendasikan](#-workflow-yang-direkomendasikan)
  - [Keamanan Trading](#-keamanan-trading)

- **[7. 🆘 Troubleshooting](#-troubleshooting)**
  - [Problem Umum](#-problem-umum)

- **[8. 🎓 Mulai Trading Pertama Anda](#-mulai-trading-pertama-anda)**
  - [Quick Start Guide](#quick-start-guide)

- **[9. 📞 Support & Community](#-support--community)**

### 🎯 Command Reference
- **Core Commands:** `*help`, `*status`, `*config`, `*mode`, `*exit`
- **Agent Commands:** `*agent market-analyst`, `*agent risk-manager`, `*agent execution-trader`, `*agent performance-tracker`
- **Team Commands:** `*team full-trading`, `*team scalping`, `*team swing-trading`
- **Trading Commands:** `*market-overview`, `*portfolio`, `*risk-check`, `*scan`, `*trade`, `*bracket-order`
- **Analysis Commands:** `*analyze`, `*signal`, `*market-dashboard`, `*market-opportunities`, `*quick-scan`
- **Workflow Commands:** `*workflow-guidance`, `*strategy [nama]`, `*signal-to-execution`, `*daily-routine`
- **Risk Commands:** `*bias-check`, `*contrarian-view`, `*reality-check`, `*emergency-mode`
- **Memory Commands:** `*memory`, `*cache-refresh`, `*session-archive`

---

## 🛠️ Persyaratan & Persiapan

### Yang Anda Butuhkan:
1. **VS Code** (versi terbaru)
2. **GitHub Copilot** (subscription aktif)
3. **Python** (versi 3.8+) - **Akan diinstall di section selanjutnya**
4. **Node.js** (versi 18+) - **Akan diinstall di section selanjutnya**
5. **Akun Binance** dengan API Key
6. **Member Key Premium** (untuk fitur premium SmartAITrading)

### 📁 Download & Setup Folder
1. Download atau clone folder `crypto-futures-core`
2. Buka folder ini di VS Code
3. Pastikan semua file `.md` dan `.yml` terbaca dengan baik

---

## 🔧 Instalasi Prerequisites (Windows)

### ⚠️ Penting: Install Dulu Sebelum Lanjut!

Sebelum menginstall sistem trading, pastikan laptop Windows Anda sudah memiliki:

#### 1. Install Python (Untuk Premium Binance MCP)

**Cara Termudah - Microsoft Store:**
1. Buka **Microsoft Store** di Windows
2. Cari "**Python**" 
3. Pilih "**Python 3.12**" (atau versi terbaru)
4. Klik "**Install**"
5. Tunggu sampai selesai

**Cara Manual - Python.org:**
1. Buka https://python.org/downloads/
2. Download "**Python 3.12**" untuk Windows
3. Jalankan installer
4. ✅ **PENTING: Centang "Add Python to PATH"**
5. Klik "Install Now"

#### 2. Install Node.js (Untuk Sequential Thinking)

**Cara Termudah - Winget:**
1. Buka **Command Prompt** atau **PowerShell** as Administrator
2. Jalankan: `winget install OpenJS.NodeJS`
3. Tunggu instalasi selesai

**Cara Manual - Node.js Website:**
1. Buka https://nodejs.org/
2. Download "**LTS version**" (yang direkomendasikan)
3. Jalankan installer
4. Klik "Next" sampai selesai (pakai setting default)

#### 3. Verifikasi Instalasi

Buka **Command Prompt** atau **PowerShell** dan cek:

```bash
# Cek Python
python --version
# Harusnya muncul: Python 3.12.x

# Cek Node.js
node --version
# Harusnya muncul: v20.x.x

# Cek npm (otomatis terinstall dengan Node.js)
npm --version
# Harusnya muncul: 10.x.x
```

#### 🚨 Troubleshooting Prerequisites

**Problem: "python is not recognized"**
```
• Restart Command Prompt/PowerShell
• Restart VS Code
• Jika masih error, reinstall Python dengan centang "Add to PATH"
```

**Problem: "node is not recognized"**
```
• Restart Command Prompt/PowerShell
• Restart VS Code
• Jika masih error, reinstall Node.js
```

**Problem: "npm is not recognized"**
```
• Node.js belum ter-install dengan benar
• Reinstall Node.js dari nodejs.org
```

---

## 🚀 Instalasi Premium Binance MCP Server

### Step 1: Install Package Python
Buka terminal di VS Code (`Ctrl + `` ` atau View > Terminal`), lalu jalankan:

```bash
pip install premium_futures_mcp
```

> 💡 **Catatan:** Jika muncul error "pip is not recognized", pastikan Python sudah ter-install dengan benar (lihat section Prerequisites di atas)

### Step 2: Konfigurasi Settings.json VS Code

1. **Buka Settings.json:**
   - Tekan `Ctrl + Shift + P`
   - Ketik "Preferences: Open User Settings (JSON)"
   - Pilih dan klik

2. **Tambahkan Konfigurasi MCP:**
   Cari bagian `"mcp"` dan tambahkan konfigurasi berikut di dalam `"servers"`:

```json
"premium-binance-futures": {
  "command": "python",
  "args": [
    "-m", 
    "premium_futures_mcp.server", 
    "--binance-api-key", "your_binance_api_key",
    "--binance-secret-key", "your_binance_secret_key",
    "--binance-member-key", "your_member_key"
  ]
}
```

3. **Tambahkan Sequential Thinking (Recommended):**
   Untuk kemampuan berpikir AI yang lebih terstruktur:

```json
"sequential-thinking": {
  "command": "npx",
  "args": [
    "-y",
    "@modelcontextprotocol/server-sequential-thinking"
  ],
  "env": {}
}
```

> 💡 **Catatan:** Sequential thinking membutuhkan Node.js. Jika muncul error "npx is not recognized", pastikan Node.js sudah ter-install (lihat section Prerequisites di atas)

### Step 3: Ganti API Keys
- **your_binance_api_key** → API Key Binance Anda
- **your_binance_secret_key** → Secret Key Binance Anda  
- **your_member_key** → Member Key Premium SmartAITrading

> 💡 **Cara Mendapatkan API Key Binance:**
> 1. Login ke akun Binance
> 2. Masuk ke API Management
> 3. Buat API Key baru
> 4. Aktifkan "Enable Futures"
> 5. Copas API Key dan Secret Key

### Step 4: Restart MCP Server
1. **Cara Cepat:** Tekan `Ctrl + Shift + P`, ketik "Developer: Reload Window"
2. **Atau:** Tutup dan buka kembali VS Code
3. **Atau:** Restart MCP di sidebar (klik tombol restart di samping server name)

---

## 🎮 Cara Menggunakan Sistem

### 1. Mulai dengan CFT Master

1. **Buka file `cft-master.md`** di folder `agents/`
2. **Buka GitHub Copilot Chat** (`Ctrl + Shift + I`)
3. **Pastikan file `cft-master.md` terbuka** - ini akan membuat Copilot memahami sistem
4. **Mulai dengan command:** `*help`

> 💡 **Update Sistem:** CFT Master sekarang merupakan unified agent yang menggabungkan fungsi trading langsung dan orchestration. Tidak perlu lagi menggunakan file orchestrator terpisah!

### 2. Command Dasar Sistem

Semua command harus dimulai dengan **asterisk (*)** di GitHub Copilot Chat:

#### 🔧 Command Utama:
```
*help              → Tampilkan semua command dan agent
*status            → Cek status pasar dan posisi saat ini
*config            → Tampilkan konfigurasi dan parameter risk
*agent [nama]      → Ubah ke agent specialist tertentu
*team [nama]       → Aktivasi tim trading (full-trading, scalping, swing-trading)
*workflow          → Mulai workflow trading
*risk-check        → Analisis risiko komprehensif
*market-overview   → Overview pasar crypto saat ini
*portfolio         → Lihat posisi dan balance
```

#### 🤖 Agent Specialists:
```
*agent market-analyst     → Analisis pasar mendalam
*agent risk-manager       → Manajemen risiko
*agent execution-trader   → Eksekusi trading
*agent performance-tracker → Tracking performa
```

#### � Team Trading:
```
*team full-trading       → Tim lengkap untuk trading komprehensif
*team scalping          → Tim untuk scalping dan high-frequency
*team swing-trading     → Tim untuk swing trading konservatif
```

#### �📊 Workflow & Market Analysis:
```
*workflow-guidance        → Panduan memilih workflow
*signal-to-execution     → Dari sinyal ke eksekusi
*daily-routine          → Rutinitas harian trading
*strategy [nama]        → Load strategi trading
*scan                   → Scan pasar 400+ token
*market-dashboard       → Dashboard pasar komprehensif
*market-opportunities   → Peluang trading dengan scoring
*quick-scan            → Scan cepat untuk peluang immediate
```

#### 🛡️ Risk & Bias Management:
```
*bias-check {symbol}     → Deteksi bias directional
*contrarian-view {symbol} → Analisis berlawanan
*reality-check {signal}  → Validasi sinyal vs data historis
*emergency-mode         → Aktivasi protokol emergency
*safe-mode             → Mode ultra-konservatif
```

### 3. Contoh Penggunaan Praktis

#### 📈 Analisis Pasar Bitcoin:
```
*agent market-analyst
Analisis kondisi pasar Bitcoin saat ini, berikan rekomendasi trading
```

#### 🎯 Analisis Peluang Trading:
```
*market-opportunities
Tampilkan peluang trading terbaik dengan scoring komprehensif
```

#### 📊 Dashboard Pasar Lengkap:
```
*market-dashboard
Tampilkan dashboard pasar dengan semua metrik penting
```

#### ⚠️ Cek Risiko Portfolio:
```
*risk-check
Evaluasi risiko portfolio saya saat ini
```

#### 🎯 Eksekusi Trading:
```
*agent execution-trader
Buat bracket order BTC long dengan TP/SL ratio 1:2
```

#### 🔍 Scan Pasar Cepat:
```
*quick-scan
Berikan analisis cepat untuk peluang trading immediate
```

#### 👥 Aktivasi Tim Trading:
```
*team full-trading
Aktivasi tim lengkap untuk trading komprehensif
```

---

## ⚙️ Kustomisasi Sistem

### 1. Mengatur Risk Profile

Edit file `data/risk-metrics.md` untuk menyesuaikan profil risiko Anda:

```yaml
# Contoh pengaturan risk yang lebih konservatif
portfolio_metrics:
  maximum_drawdown:
    threshold: 10.0  # Ubah dari 20% ke 10%
    
position_metrics:
  position_size:
    max_portfolio_percentage: 5.0  # Ubah dari 10% ke 5%
```

### 2. Mengatur Technical Indicators

Edit file `data/technical-indicators.md` untuk menyesuaikan indikator:

```yaml
# Contoh: Ubah setting RSI
momentum_indicators:
  rsi:
    period: 21        # Ubah dari 14 ke 21
    overbought: 75    # Ubah dari 70 ke 75
    oversold: 25      # Ubah dari 30 ke 25
```

### 3. Membuat Strategy Custom

1. Buka folder `strategies/`
2. Copy file `strategy-template.md`
3. Edit sesuai kebutuhan
4. Gunakan dengan command `*strategy [nama-file]`

---

## 🔥 Tips & Trik Penggunaan

### 💪 Best Practices:
1. **Selalu mulai dengan `*help`** untuk melihat command terbaru
2. **Gunakan `*config`** untuk melihat parameter risk saat ini
3. **Gunakan `*risk-check`** sebelum trading besar
4. **Aktifkan `*agent risk-manager`** untuk monitoring otomatis
5. **Gunakan `*scan`** untuk mencari peluang trading di banyak token
6. **Manfaatkan `*market-dashboard`** untuk overview pasar lengkap
7. **Gunakan `*team [nama]`** untuk aktivasi tim trading sesuai strategi
8. **Aktifkan `*bias-check`** untuk deteksi bias sebelum trading
9. **Save analisis penting** dengan `*memory`
10. **Gunakan `*quick-scan`** untuk peluang immediate

### 🎯 Workflow yang Direkomendasikan:
1. **Morning Routine:**
   ```
   *market-overview
   *portfolio
   *risk-check
   *market-dashboard
   ```

2. **Analisis Trading:**
   ```
   *agent market-analyst
   *market-opportunities
   *scan
   *workflow-guidance
   ```

3. **Persiapan Trading:**
   ```
   *bias-check [symbol]
   *contrarian-view [symbol]
   *reality-check [signal]
   ```

4. **Eksekusi Trading:**
   ```
   *agent execution-trader
   *checklist pre-trade-checklist
   *bracket-order [symbol] [side] [size] [tp] [sl]
   ```

5. **Tim Trading (Advanced):**
   ```
   *team full-trading      → Untuk trading komprehensif
   *team scalping         → Untuk high-frequency trading
   *team swing-trading    → Untuk position trading
   ```

### 🚨 Keamanan Trading:
- **Jangan share API Keys** dengan siapa pun
- **Gunakan IP whitelist** di Binance API settings
- **Set limit harian** untuk trading otomatis
- **Selalu backup** konfigurasi penting

---

## 🆘 Troubleshooting

### ❌ Problem Umum:

**1. MCP Server tidak connect:**
```
• Cek apakah API keys sudah benar
• Restart VS Code
• Cek koneksi internet
• Pastikan Python package ter-install
```

**2. Command tidak berfungsi:**
```
• Pastikan file cft-master.md terbuka
• Gunakan * di depan command
• Cek ejaan command
• Restart GitHub Copilot
• Pastikan MCP server terhubung
```

**3. Error saat trading:**
```
• Cek balance Binance
• Pastikan API key punya akses Futures
• Cek status pasar (maintenance?)
• Gunakan *risk-check
```

---

## 🎓 Mulai Trading Pertama Anda

### Quick Start Guide:
1. **Buka `cft-master.md`**
2. **Mulai chat dengan:** `*help`
3. **Cek kondisi:** `*market-overview`
4. **Lihat dashboard:** `*market-dashboard`
5. **Pilih agent:** `*agent market-analyst`
6. **Minta analisis:** "Analisis peluang trading hari ini"
7. **Cek peluang:** `*market-opportunities`
8. **Validasi bias:** `*bias-check [symbol]`
9. **Eksekusi:** `*agent execution-trader`
10. **Aktivasi tim:** `*team full-trading` (untuk trading komprehensif)

### 🎯 Selamat Trading!
Dengan CFT Master yang telah di-upgrade, Anda memiliki AI trading assistant yang lebih powerful dan unified. Sistem ini menggabungkan kemampuan trading langsung dengan orchestration agent yang cerdas. Mulai dari analisis pasar hingga eksekusi trading, semuanya bisa dilakukan dengan mudah melalui satu agent utama.

### 🆕 Fitur Baru CFT Master:
- **Unified Agent**: Satu agent untuk semua kebutuhan trading
- **Team Management**: Koordinasi tim trading otomatis
- **Advanced Market Analysis**: Dashboard dan opportunities dengan scoring
- **Enhanced Risk Management**: Bias detection dan reality check
- **Workflow Orchestration**: Panduan workflow yang lebih cerdas
- **Memory & Cache Management**: Sistem memory yang lebih baik

> **⚠️ Disclaimer:** Trading crypto futures memiliki risiko tinggi. Selalu gunakan manajemen risiko yang baik dan jangan trading dengan uang yang tidak mampu Anda rugi.

---

## 📞 Support & Community

Untuk pertanyaan lebih lanjut atau bergabung dengan komunitas premium, hubungi **SmartAITrading** untuk mendapatkan member key premium.

**Happy Trading! 🚀**
