FARUK AI PHOTO STUDIO — প্রাথমিক PWA সংস্করণ

এই প্যাকেজে আছে:
- index.html: মোবাইল-ফ্রেন্ডলি ওয়েব অ্যাপ
- manifest.json: Home Screen install পরিচিতি
- sw.js: Service Worker / basic offline caching
- icon.svg: অ্যাপ আইকন

চালানোর নিয়ম:
১) ZIP ফাইলটি Extract করুন।
২) ফাইলগুলো একসাথে কোনো HTTPS static hosting-এ আপলোড করুন (যেমন GitHub Pages বা Netlify-এর free tier)।
৩) প্রকাশিত HTTPS লিংক Android Chrome-এ খুলুন।
৪) Chrome menu থেকে Install app / Add to Home screen নির্বাচন করুন।

সীমাবদ্ধতা:
এটি প্রথম কার্যকর প্রোটোটাইপ। অটোমেটিক কালার, আলো, কনট্রাস্ট ও হালকা শার্পনেস উন্নত করে।
এখনো প্রকৃত AI segmentation-ভিত্তিক DSLR background blur, face-specific enhancement এবং AI upscaling যুক্ত হয়নি।
এই সংস্করণে ছবি ব্রাউজারেই প্রসেস হয়; কোনো সার্ভারে আপলোড করা হয় না।
