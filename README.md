# node-app

A Node.js Express web application containerized with Docker and integrated with a Jenkins CI pipeline — automatically tested and triggered on every GitHub push via webhook.

---

## Pipeline Flow

```
git push → GitHub Webhook → Jenkins triggered
                                    ↓
                            Checkout → Install → Test (Jest)
                                    ↓
                            Build passes → Green ✓
```

---

## Tech Stack

| Tool | Role |
|---|---|
| Node.js + Express | Web application |
| Jest | Unit testing |
| Docker | Containerization |
| Jenkins | CI automation |
| GitHub Webhooks | Auto-trigger on push |

---

## Project Structure

```
node-app/
├── app.js          # Express web server
├── app.test.js     # Jest unit tests
├── Dockerfile      # Container build instructions
└── package.json    # Node dependencies
```

---

## Run with Docker

```bash
docker pull kushal81/my-node-app
docker run -d -p 3000:3000 kushal81/my-node-app
```

Open browser → `http://localhost:3000`

---

## Author

**Kushal Sapkota**  
[GitHub](https://github.com/Kushal-Sapkota) · [LinkedIn](https://linkedin.com/in/kushal-sapkota) · [Portfolio](https://kushalsapkota81.com.np)