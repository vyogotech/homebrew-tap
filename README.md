# Vyogotech Homebrew Tap

Official Homebrew tap for Vyogo Technologies packages and server stacks.

## Available Formulae

| Formula | Description | Install |
| :--- | :--- | :--- |
| [`vybench`](Formula/vybench.rb) | Frappe Bench v16 & ERPNext v16 single-node server stack for macOS | `brew install vyogotech/tap/vybench` |

---

## Installation & Usage

### 1. Add the Tap

```bash
brew tap vyogotech/tap
```

### 2. Install Vybench

```bash
brew install vybench
```

### 3. Start Required Services

```bash
# Start backend datastores
brew services start mariadb
brew services start redis

# Start the Vybench application stack
brew services start vybench
```

### 4. Create Your First Site

```bash
vybench bench new-site mysite.localhost --admin-password admin
```

Access your site at `http://mysite.localhost:8000`.

---

## Service Management

```bash
# Check service status
brew services list

# Restart the application stack
brew services restart vybench

# Stop the application stack
brew services stop vybench
```

---

## Documentation & Support

- **Repository & Docs:** [vyogotech/vybench](https://github.com/vyogotech/vybench)
- **Issue Tracker:** [vyogotech/vybench/issues](https://github.com/vyogotech/vybench/issues)
