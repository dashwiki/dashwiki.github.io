# [ডেবিয়ান] Debian Almquist Shell (dash) true ব্যবহার: সত্য মান প্রদান করে

## Overview
`true` কমান্ডটি একটি খুব সহজ এবং মৌলিক কমান্ড যা সর্বদা সফলভাবে সম্পন্ন হয়। এটি সাধারণত স্ক্রিপ্টে ব্যবহৃত হয় যেখানে একটি সফল অবস্থার প্রয়োজন হয়।

## Usage
নিচে `true` কমান্ডের মৌলিক সিনট্যাক্স দেওয়া হলো:

```bash
true [options] [arguments]
```

## Common Options
`true` কমান্ডের জন্য সাধারণত কোন অপশন নেই, কারণ এটি শুধুমাত্র সফলভাবে সম্পন্ন হয় এবং কোন আর্গুমেন্ট গ্রহণ করে না।

## Common Examples
নিচে কিছু সাধারণ উদাহরণ দেওয়া হলো:

### উদাহরণ 1: স্ক্রিপ্টে ব্যবহার
```bash
if true; then
  echo "এটি সফল হয়েছে!"
fi
```

### উদাহরণ 2: লুপে ব্যবহার
```bash
while true; do
  echo "এটি চলতে থাকবে!"
  sleep 1
done
```

### উদাহরণ 3: পাসওয়ার্ড যাচাই
```bash
if true; then
  echo "পাসওয়ার্ড সঠিক।"
else
  echo "পাসওয়ার্ড ভুল।"
fi
```

## Tips
- `true` কমান্ডটি সাধারণত স্ক্রিপ্টে একটি সফল অবস্থার জন্য ব্যবহৃত হয়, তাই এটি ব্যবহার করার সময় নিশ্চিত করুন যে এটি আপনার প্রয়োজন অনুযায়ী কাজ করছে।
- এটি `false` কমান্ডের বিপরীত, তাই আপনি যখন `false` ব্যবহার করতে চান তখন `true` ব্যবহার করতে পারেন সফল অবস্থার জন্য।