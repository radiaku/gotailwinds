# GoTailwinds

A modern Go web app starter using [Templ](https://templ.guide/), [Tailwind CSS](https://tailwindcss.com/), and [Air](https://github.com/cosmtrek/air) for live reloading.

## 📦 Prerequisites

- [Go](https://golang.org/doc/install)
- [Node.js + npm](https://nodejs.org/)
- [Air](https://github.com/cosmtrek/air): Live-reload for Go apps  
  Install via:

  ```sh
  go install github.com/cosmtrek/air@latest
  ```

---

## 🚀 Quick Start

### 1. Clone and Install Dependencies

```sh
git clone https://github.com/radiaku/gotailwinds.git
cd gotailwinds
make install
```

This will:
- Install `templ` (Go HTML templating tool)
- Install TailwindCSS
- Initialize npm
- Create `bin/` directory

---

### 2. Configure `.env`

Create a `.env` file in the root with:

```env
APP_PORT=8080
TEMPL_PROXY_PORT=8787
```

---

### 3. Initialize Tailwind

```sh
make init
```

This will:
- Create `tailwind.config.js`
- Setup `static/css/tailwind.css`
- Run Tailwind in dev mode

---

### 4. Run the App

```sh
make run
```

This will:
- Start `templ` in watch mode
- Start the Go server with `air` for live reload

### 5. Run and watch tailwinds changes

```sh
make tailwind
```

---

## 🔨 Other Make Targets

| Command             | Description                                          |
|----------------------|------------------------------------------------------|
| `make build`         | Build production binary in `bin/`                    |
| `make build-local`   | Build binary to `bin/main`                           |
| `make templ`         | Run `templ generate` with live proxy (watch mode)    |
| `make tailwind`      | Watch the tailwinds                                    |
| `make notify`        | Notify proxy-only templ generate mode                |

---

## 📁 Project Structure

```
gotailwinds/
├── cmd/
│   └── main/           # Main entry point
├── static/             # Static files (CSS, JS, images)
├── view/               # Templ view components
│   ├── layout/
│   └── partial/
├── bin/                # Build output
├── .env
├── makefile
└── README.md
```

---

## ★ Demo
https://github.com/radiaku/gotailwindsdemo

---
## 📄 License

MIT
