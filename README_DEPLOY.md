# Deploy to Cloudflare Pages

1. Buy domain in Cloudflare > Domain Registration
2. Create Pages project: Cloudflare Dashboard > Pages > Create a project > Direct Upload
3. Drag this entire folder (index.html + favicon files)
4. In Custom Domains > Add your domain
5. For real global counter:
   - Create Worker: Cloudflare > Workers & Pages > Create Worker > paste worker.js from earlier message
   - Create KV namespace COUNTER, bind to worker as env.COUNTER
   - Copy worker URL into index.html line: const WORKER_URL = 'https://...'
   - Redeploy

For private analytics (recommended): Dashboard > Web Analytics > Add site > copy beacon token into the commented script at bottom of index.html

Done!
