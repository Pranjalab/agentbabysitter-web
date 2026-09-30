# IndexNow

Bing (and Yandex, Naver, Seznam) accept a ping when a URL changes instead of
waiting to re-crawl. The key is the filename in this directory: it must stay
served at the site root, unchanged, or submissions are rejected.

Key: `0feefee4f44052339545d058a493d462`
Key file: `https://agentbabysitter.com/0feefee4f44052339545d058a493d462.txt`

Submit the whole site after a deploy — one request, up to 10,000 URLs:

    curl -sS -X POST 'https://api.indexnow.org/indexnow' \
      -H 'Content-Type: application/json; charset=utf-8' \
      -d '{
        "host": "agentbabysitter.com",
        "key": "0feefee4f44052339545d058a493d462",
        "keyLocation": "https://agentbabysitter.com/0feefee4f44052339545d058a493d462.txt",
        "urlList": [
          "https://agentbabysitter.com/",
          "https://agentbabysitter.com/features.html",
          "https://agentbabysitter.com/docs.html",
          "https://agentbabysitter.com/faq.html",
          "https://agentbabysitter.com/about.html",
          "https://agentbabysitter.com/releases.html",
          "https://agentbabysitter.com/security.html"
        ]
      }'

A 200 or 202 means accepted. Google does not participate in IndexNow; for Google,
the sitemap in Search Console is the equivalent.
