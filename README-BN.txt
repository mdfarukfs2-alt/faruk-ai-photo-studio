FARUK AI PHOTO STUDIO — AI upgrade package (beta)

ফাইল:
- index.html: আপগ্রেড করা মোবাইল-ফ্রেন্ডলি এডিটর
- manifest.json: PWA metadata
- sw.js: basic same-origin cache
- icon.svg: app icon

GitHub Pages-এ আপডেট:
1) ZIP extract করুন।
2) GitHub repository খুলুন → Add file → Upload files।
3) ZIP-এর ভেতরের চারটি ফাইল (index.html, manifest.json, sw.js, icon.svg) repository-র মূল root-এ upload করুন; ZIP ফাইলটি নিজে upload করলে সাইটের ফাইল বদলাবে না।
4) index.html overwrite/replace করুন, তারপর Commit changes চাপুন।
5) Pages deploy হওয়ার পর ওয়েবসাইট খুলে browser cache clear/refresh করুন। Android Chrome-এ দরকার হলে site data/cache clear করে আবার খুলুন।

AI মডেল:
- Background removal/matting: Xenova/modnet via Transformers.js (Apache-2.0 model card).
- Super-resolution: onnx-community/swin2SR-classical-sr-x2-64 via Transformers.js.
মডেলগুলো প্রথমবার Hugging Face/CDN থেকে ডাউনলোড হয়; তাই ইন্টারনেট ও বড় ডাউনলোড প্রয়োজন। মডেল/ব্রাউজার/ডিভাইস অনুযায়ী ব্যর্থ হতে পারে। ছবির প্রসেসিং ব্রাউজারে হয়, তবে মডেল ফাইল তৃতীয়-পক্ষের CDN/repository থেকে ডাউনলোড হয়।

সততা ও সীমাবদ্ধতা:
- এই প্যাকেজে background blur ও super-resolution-এ প্রকৃত pretrained model inference যুক্ত করার চেষ্টা আছে, কিন্তু এই পরিবেশে Android/browser-এ runtime inference চালিয়ে যাচাই করা সম্ভব হয়নি। সাইটে আপলোডের পর প্রতিটি মডেল বাস্তবে পরীক্ষা করুন।
- Color Enhance হলো pixel-based correction, AI model নয়।
- Face Detail Enhance হলো conservative sharpening; প্রকৃত GFPGAN/CodeFormer face restoration model এখনো সংযুক্ত নয়। একে AI face restoration বলা হচ্ছে না।
- Upscale এবং Restoration একই Swin2SR super-resolution model ব্যবহার করে; এটি সাধারণ super-resolution, পূর্ণাঙ্গ damaged-photo restoration নয়।
- কোনো paid API key নেই; CDN ও model repository ব্যবহারে ব্যবহারকারীর নেট সংযোগ/ডেটা লাগবে।
