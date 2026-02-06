# Test the site locally

## 1. Use Ruby 3

Your Mac’s built-in Ruby is 2.6; Jekyll’s dependencies need **Ruby 3.0 or newer**.

**Option A – Homebrew (simple)**  
```bash
brew install ruby
```
Then use the Homebrew Ruby (add to your `~/.zshrc` if needed):
```bash
echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

**Option B – rbenv (per-project Ruby)**  
```bash
brew install rbenv ruby-build
rbenv install 3.2.0
rbenv local 3.2.0   # in this repo
```

Check:
```bash
ruby --version   # should be 3.x
```

## 2. Install dependencies

```bash
cd /Users/kylie/Documents/GitHub/kjm1425.github.io
bundle install
```

## 3. Serve the site

```bash
bundle exec jekyll serve
```

Open **http://localhost:4000** in your browser. Edit content or styles and refresh to see changes (Sass may need a restart).

To listen on all interfaces (e.g. test on your phone on the same Wi‑Fi):
```bash
bundle exec jekyll serve --host 0.0.0.0
```
