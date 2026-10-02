Vercel structure

api/       serverless Python entrypoints
lib/       backend implementation (kept outside root so Vercel does not treat it as an entrypoint)
index.html must remain in the project root.

Add GEMINI_API_KEY in Vercel Project Settings -> Environment Variables.
Do not commit your real .env file.

After copying these files:
1. Keep your existing index.html in the root.
2. Remove the old root backend.py/server.py files.
3. git add .
4. git commit -m "Fix Vercel Python deployment"
5. git push origin main
