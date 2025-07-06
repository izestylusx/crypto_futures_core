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
  - [Konfigurasi Utama - core-config.yml](#1-konfigurasi-utama---core-configyml)
  - [Contoh Kustomisasi untuk Berbagai Profil Trader](#2-contoh-kustomisasi-untuk-berbagai-profil-trader)
  - [Optimasi Performance & Resource](#3-optimasi-performance--resource)
  - [Sistem Memory Fleksibel](#4-sistem-memory-fleksibel)
  - [Cara Menerapkan Kustomisasi](#5-cara-menerapkan-kustomisasi)
  - [Parameter Baru yang Ditambahkan](#6-parameter-baru-yang-ditambahkan)
  - [Sistem Dokumentasi Otomatis](#7-sistem-dokumentasi-otomatis-baru)
  - [Membuat Strategy Custom](#8-membuat-strategy-custom)

- **[6. 🔥 Tips & Trik Penggunaan](#-tips--trik-penggunaan)**
  - [Best Practices](#-best-practices)
  - [Workflow yang Direkomendasikan](#-workflow-yang-direkomendasikan)
  - [Keamanan Trading](#-keamanan-trading)

- **[7. 🆘 Troubleshooting](#-troubleshooting)**
  - [Problem Umum](#-problem-umum)

- **[8. 🎓 Mulai Trading Pertama Anda](#-mulai-trading-pertama-anda)**
  - [Quick Start Guide](#quick-start-guide)
  - [Selamat Trading](#-selamat-trading)
  - [Fitur Baru CFT Master](#-fitur-baru-cft-master)

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
- **Documentation Commands:** `*generate-docs`, `*auto-docs`, `*session-docs`, `*daily-docs`, `*docs-index`

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
• Check PATH environment variable
• Jika masih error, reinstall Python dengan centang "Add to PATH"
```

**Problem: "node is not recognized"**
```
• Restart Command Prompt/PowerShell
• Check PATH environment variable
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
1. **Cara Cepat:** Restart MCP di sidebar (klik tombol restart di samping server name)
2. **Atau:** Tutup dan buka kembali VS Code
3. **Atau:** Tekan `Ctrl + Shift + P`, ketik "Developer: Reload Window"

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
*portfolio         → Lihat posisi dan balance
*market-overview   → Overview pasar crypto saat ini
*status            → Status sistem dan performance
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

### 1. Konfigurasi Utama - core-config.yml

File `core-config.yml` adalah pusat konfigurasi sistem yang akan dibaca oleh CFT Master dan semua agent. Edit file ini untuk menyesuaikan sistem sesuai kebutuhan:

```yaml
# Trading Configuration - DAPAT DIUBAH SESUAI KEBUTUHAN
trading:
  exchange: "binance_futures"
  default_leverage: 5           # Leverage default (1-20)
  max_leverage: 20             # Maksimal leverage yang diizinkan
  risk_percentage: 2.0         # Persentase risiko per trade (1.0-5.0)
  base_currency: "USDT"        # Mata uang dasar
  
  # Trading Modes - BARU!
  paper_trading: false         # Mode paper trading (simulasi)
  auto_trading: false          # Trading otomatis
  max_daily_trades: 20         # Maksimal trade per hari
  max_open_positions: 10       # Maksimal posisi terbuka
  
  # Order Management - BARU!
  order_timeout: 300           # Timeout order dalam detik
  slippage_tolerance: 0.5      # Toleransi slippage (%)
  partial_fill_threshold: 0.8  # Minimum fill ratio

# Risk Management - SESUAIKAN DENGAN PROFIL RISIKO ANDA
risk_management:
  max_portfolio_risk: 10.0     # Maksimal risiko portfolio (5.0-20.0)
  max_position_risk: 5.0       # Maksimal risiko per posisi (2.0-10.0)
  stop_loss_percentage: 2.0    # Persentase stop loss (1.0-5.0)
  take_profit_ratio: 2.0       # Ratio take profit (1.5-3.0)
  max_drawdown_threshold: 20.0 # Threshold maksimal drawdown (10.0-30.0)
  
  # Advanced Risk Controls - BARU!
  correlation_limit: 0.7       # Maksimal korelasi antar posisi
  sector_exposure_limit: 30.0  # Maksimal eksposur per sektor
  volatility_adjustment: true  # Sesuaikan ukuran posisi berdasarkan volatilitas
  
  # Emergency Controls - BARU!
  emergency_stop_loss: 15.0    # Emergency stop loss (%)
  margin_call_threshold: 80.0  # Threshold margin call
  force_close_threshold: 90.0  # Threshold force close

# Memory System - FLEKSIBEL UNTUK SEMUA USER
memory_system:
  # OpenMemory MCP (Opsional - butuh instalasi terpisah)
  use_openmemory: false        # Aktifkan OpenMemory jika tersedia
  
  # File-based Memory (Selalu tersedia)
  use_file_memory: true        # Memory berbasis file
  cache_duration: 300          # Durasi cache dalam detik (60-600)
  file_documentation: true     # Dokumentasi file otomatis
  session_tracking: true       # Tracking session
  
  # Memory Management - BARU!
  max_memory_entries: 1000     # Maksimal entry memory
  memory_cleanup_interval: 3600 # Interval cleanup (detik)
  compress_old_data: true      # Kompresi data lama

# Performance Optimization - BARU!
performance:
  # Market Data
  market_data_interval: 1000   # Interval refresh data pasar (ms)
  max_symbols_scan: 400        # Maksimal simbol untuk scan
  concurrent_requests: 10      # Maksimal request bersamaan
  
  # Analysis Optimization
  enable_caching: true         # Aktifkan cache analisis
  cache_analysis_duration: 180 # Cache analisis selama 3 menit
  parallel_analysis: true      # Analisis paralel
  
  # Resource Management
  max_cpu_usage: 80           # Maksimal penggunaan CPU (%)
  max_memory_usage: 70        # Maksimal penggunaan memory (%)

# Market Scanning Configuration - BARU!
market_scanning:
  # Filtering
  min_volume_24h: 1000000     # Minimum volume 24h
  min_price: 0.0001           # Minimum harga
  max_price: 100000           # Maksimum harga
  
  # Scanning Intervals
  quick_scan_interval: 30     # Interval quick scan (detik)
  deep_scan_interval: 300     # Interval deep scan (detik)
  
  # Opportunity Detection
  min_opportunity_score: 20   # Minimum skor peluang
  max_opportunities: 50       # Maksimal peluang untuk tracking

# Notification System - BARU!
notifications:
  # Alert Settings
  enable_alerts: true         # Aktifkan alert sistem
  alert_sound: true           # Suara alert
  desktop_notifications: true # Notifikasi desktop
  
  # Alert Thresholds
  profit_alert_threshold: 5.0 # Threshold alert profit
  loss_alert_threshold: 3.0   # Threshold alert loss
  volume_spike_threshold: 3.0 # Threshold spike volume
```

### 2. Contoh Kustomisasi untuk Berbagai Profil Trader

#### 🔰 Profil Konservatif (Pemula):
```yaml
trading:
  default_leverage: 3
  risk_percentage: 1.0
  paper_trading: true          # Mulai dengan simulasi
  max_daily_trades: 5          # Batasi jumlah trade

risk_management:
  max_portfolio_risk: 5.0
  max_position_risk: 2.0
  stop_loss_percentage: 1.5
  max_drawdown_threshold: 10.0
  emergency_stop_loss: 10.0    # Stop loss emergency lebih ketat

performance:
  max_symbols_scan: 50         # Scan token terbatas
  concurrent_requests: 3       # Request lebih sedikit
```

#### ⚡ Profil Agresif (Berpengalaman):
```yaml
trading:
  default_leverage: 10
  risk_percentage: 3.0
  auto_trading: true           # Trading otomatis
  max_daily_trades: 50         # Lebih banyak trade
  max_open_positions: 20       # Lebih banyak posisi

risk_management:
  max_portfolio_risk: 15.0
  max_position_risk: 8.0
  stop_loss_percentage: 3.0
  max_drawdown_threshold: 25.0
  correlation_limit: 0.8       # Toleransi korelasi lebih tinggi

performance:
  max_symbols_scan: 400        # Scan semua token
  concurrent_requests: 15      # Request lebih banyak
  parallel_analysis: true      # Analisis paralel
```

#### 🏃 Profil Scalping (High-Frequency):
```yaml
trading:
  default_leverage: 20
  risk_percentage: 1.5
  max_daily_trades: 100        # Banyak trade harian
  order_timeout: 60            # Timeout order lebih cepat
  slippage_tolerance: 0.1      # Toleransi slippage ketat

risk_management:
  max_portfolio_risk: 8.0
  max_position_risk: 3.0
  stop_loss_percentage: 1.0
  take_profit_ratio: 1.5       # TP/SL ratio lebih kecil

performance:
  market_data_interval: 500    # Refresh data lebih cepat
  concurrent_requests: 20      # Request lebih banyak
  
market_scanning:
  quick_scan_interval: 10      # Scan lebih sering
  min_opportunity_score: 15    # Threshold peluang lebih rendah
```

### 3. Optimasi Performance & Resource

#### 🚀 Mode High Performance:
```yaml
performance:
  enable_caching: true
  cache_analysis_duration: 300
  parallel_analysis: true
  max_cpu_usage: 90
  max_memory_usage: 80
  
market_scanning:
  max_symbols_scan: 500
  concurrent_requests: 20
  quick_scan_interval: 15
```

#### 💾 Mode Low Resource (Laptop Lambat):
```yaml
performance:
  enable_caching: true
  cache_analysis_duration: 600  # Cache lebih lama
  parallel_analysis: false      # Nonaktifkan paralel
  max_cpu_usage: 50
  max_memory_usage: 40
  
market_scanning:
  max_symbols_scan: 100         # Scan lebih sedikit
  concurrent_requests: 3        # Request lebih sedikit
  quick_scan_interval: 60       # Scan lebih jarang
```

### 4. Sistem Memory Fleksibel

#### 📚 Dengan OpenMemory MCP (Jika Tersedia):
```yaml
memory_system:
  use_openmemory: true         # Aktifkan jika terinstall
  use_file_memory: true        # Backup dengan file
  cache_duration: 300
  max_memory_entries: 2000
```

#### 📁 Tanpa OpenMemory MCP (Default):
```yaml
memory_system:
  use_openmemory: false        # Nonaktifkan
  use_file_memory: true        # Andalkan file memory
  cache_duration: 600          # Cache lebih lama
  max_memory_entries: 1000
  compress_old_data: true      # Kompresi untuk efisiensi
```

### 5. Cara Menerapkan Kustomisasi

1. **Edit file `core-config.yml`** di root folder
2. **Save file** (`Ctrl + S`) - perubahan akan otomatis terbaca oleh sistem
3. **Jalankan `*config`** di CFT Master untuk memverifikasi parameter yang dimuat
4. **Test dengan `*status`** untuk memastikan sistem berjalan dengan konfigurasi baru
5. **Monitor performance** dengan `*market-overview` atau `*portfolio`

### 6. Parameter Baru yang Ditambahkan

#### 🎯 Trading Enhancement:
- **Paper Trading Mode**: Simulasi trading tanpa risiko
- **Auto Trading**: Trading otomatis berdasarkan sinyal
- **Order Management**: Timeout dan slippage control
- **Position Limits**: Kontrol jumlah posisi dan trade harian

#### 🛡️ Advanced Risk Management:
- **Correlation Limits**: Hindari posisi yang berkorelasi tinggi
- **Sector Exposure**: Batasi eksposur per sektor
- **Emergency Controls**: Protokol emergency otomatis
- **Volatility Adjustment**: Sesuaikan ukuran posisi berdasarkan volatilitas

#### ⚡ Performance Optimization:
- **Caching System**: Cache analisis untuk efisiensi
- **Parallel Processing**: Analisis paralel untuk kecepatan
- **Resource Management**: Kontrol penggunaan CPU dan memory
- **Concurrent Requests**: Optimasi request API

#### � Market Scanning Enhancement:
- **Advanced Filtering**: Filter volume, harga, dan kriteria lain
- **Flexible Intervals**: Sesuaikan interval scanning
- **Opportunity Detection**: Scoring dan tracking peluang
- **Tier-based Analysis**: Analisis berdasarkan tier token

#### 🔔 Notification System:
- **Multi-channel Alerts**: Desktop, sound, dan webhook
- **Customizable Thresholds**: Atur threshold sesuai kebutuhan
- **Real-time Alerts**: Notifikasi real-time untuk event penting

### 7. Sistem Dokumentasi Otomatis (BARU!)

Sistem ini akan menggunakan GitHub Copilot untuk membuat dokumentasi otomatis dari semua aktivitas trading Anda:

```yaml
# Documentation System - AUTOMATIC DOCUMENTATION GENERATION
documentation:
  # Auto Documentation Settings
  auto_documentation: true     # Aktifkan dokumentasi otomatis
  documentation_trigger: "analysis_complete"  # Kapan membuat dokumentasi
  documentation_format: "markdown"  # Format dokumentasi (markdown/json/yaml)
  
  # Documentation Types
  generate_analysis_docs: true    # Dokumentasi analisis
  generate_trade_docs: true       # Dokumentasi trading
  generate_session_docs: true     # Dokumentasi session
  generate_strategy_docs: true    # Dokumentasi strategi
  generate_performance_docs: true # Dokumentasi performa
  
  # Documentation Triggers - KAPAN DOKUMENTASI DIBUAT
  triggers:
    after_analysis: true          # Setelah analisis pasar
    after_trade: true             # Setelah eksekusi trade
    after_session: true           # Setelah session berakhir
    daily_summary: true           # Rangkuman harian
    
  # Documentation Locations - DIMANA DOKUMENTASI DISIMPAN
  locations:
    analysis_docs: "docs/analysis/"     # Folder dokumentasi analisis
    trade_docs: "docs/trades/"          # Folder dokumentasi trading
    session_docs: "docs/sessions/"      # Folder dokumentasi session
    strategy_docs: "docs/strategies/"   # Folder dokumentasi strategi
    performance_docs: "docs/performance/" # Folder dokumentasi performa
```

#### 📋 Jenis Dokumentasi yang Dihasilkan:

1. **📊 Analysis Documentation** - Dibuat setelah analisis pasar
   - Kondisi pasar saat analisis
   - Indikator teknikal yang digunakan
   - Temuan dan insight utama
   - Rekomendasi trading
   - Deteksi bias
   - File: `docs/analysis/YYYY-MM-DD_HH-MM_analysis_{symbol}.md`

2. **💰 Trade Documentation** - Dibuat setelah eksekusi trading
   - Setup dan reasoning trade
   - Harga entry/exit dan timing
   - Ukuran posisi dan kalkulasi risk
   - Kondisi pasar saat trading
   - Hasil trade dan lessons learned
   - File: `docs/trades/YYYY-MM-DD_HH-MM_trade_{symbol}_{side}.md`

3. **📅 Session Documentation** - Dibuat di akhir session
   - Overview dan objektif session
   - Pasar yang dianalisis dan ditrade
   - Ringkasan performa
   - Keputusan kunci yang dibuat
   - Lessons learned
   - File: `docs/sessions/YYYY-MM-DD_session_summary.md`

4. **🎯 Strategy Documentation** - Dibuat setelah menjalankan strategi
   - Deskripsi strategi dan parameter
   - Metrik performa
   - Kondisi pasar yang ditest
   - Success/failure rates
   - Optimasi yang dilakukan
   - File: `docs/strategies/YYYY-MM-DD_{strategy_name}_performance.md`

#### 🤖 Cara Kerja Dokumentasi Otomatis:

1. **Event Detection** - Sistem mendeteksi completion event (analisis selesai, trade dieksekusi, dll.)
2. **Data Collection** - Mengumpulkan data dari cache dan memory
3. **Template Loading** - Load template dokumentasi yang sesuai
4. **AI Generation** - GitHub Copilot menghasilkan dokumentasi lengkap
5. **File Creation** - Membuat file markdown dengan naming yang terstandar
6. **Index Update** - Update index dokumentasi secara otomatis

#### 📝 Command Dokumentasi:

```
# Manual Documentation Generation
*generate-docs analysis     → Generate dokumentasi analisis
*generate-docs trade        → Generate dokumentasi trading
*generate-docs session      → Generate dokumentasi session
*session-docs              → Generate dokumentasi session saat ini
*daily-docs                → Generate rangkuman harian

# Documentation Management
*auto-docs on              → Aktifkan dokumentasi otomatis
*auto-docs off             → Matikan dokumentasi otomatis
*docs-index                → Generate/update index dokumentasi
*docs-cleanup              → Bersihkan dokumentasi lama
*docs-archive              → Archive dokumentasi lama
```

#### 💡 Keuntungan Sistem Dokumentasi Otomatis:

- **📈 Pembelajaran Berkelanjutan** - Dokumentasi lengkap untuk review dan improvement
- **🔍 Analisis Performa** - Tracking performa trading secara detail
- **🛡️ Compliance** - Dokumentasi untuk kebutuhan regulasi
- **🧠 Knowledge Base** - Membangun knowledge base dari pengalaman trading
- **🔄 Iterasi Strategi** - Dokumentasi untuk mengoptimalkan strategi
- **📊 Portfolio Review** - Review portfolio secara komprehensif

> 💡 **Fitur Unggulan**: Sistem ini menggunakan GitHub Copilot untuk menghasilkan dokumentasi yang sangat detail dan terstruktur, membantu Anda memahami dan meningkatkan performa trading secara berkelanjutan!

### 8. Membuat Strategy Custom

1. Buka folder `strategies/`
2. Copy file `strategy-template.md`
3. Edit sesuai kebutuhan
4. Gunakan dengan command `*strategy [nama-file]`

> 💡 **Catatan Penting:** Sistem sekarang lebih fleksibel dan tidak bergantung pada OpenMemory MCP. Semua user bisa menggunakan file-based memory sebagai default, dan yang memiliki OpenMemory MCP bisa mengaktifkannya sebagai enhancement.

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
• Restart MCP server di sidebar
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
• Gunakan *status untuk cek kondisi sistem
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
