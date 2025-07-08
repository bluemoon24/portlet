# Running `simple.html` Locally

You can view the `simple.html` example page locally by serving it with a simple HTTP server. Follow these steps:

## 1. Navigate to the Directory

Open your terminal and change to the directory containing `simple.html`:

```bash
cd /Users/lothar/Documents/projects/efds-roi5-portletce/packages/portletce/public/examples
```

## 2. Start a Local Server

If you have Python installed (default on macOS), run:

```bash
python3 -m http.server 8000
```

This will start a server at [http://localhost:8000](http://localhost:8000).

## 3. Open the Page in Your Browser

Go to:

```
http://localhost:8000/simple.html
```

---

**Alternative:**  
If you have Node.js installed, you can use `npx serve` or `npx http-server`:

```bash
npx serve .
# or
npx http-server .
```
