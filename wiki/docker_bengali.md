# [লিনাক্স] C Shell (csh) docker ব্যবহার: কনটেইনার পরিচালনা করা

## Overview
ডকার একটি ওপেন সোর্স প্ল্যাটফর্ম যা ডেভেলপারদের কনটেইনারে অ্যাপ্লিকেশন তৈরি, বিতরণ এবং চালানোর সুবিধা দেয়। এটি বিভিন্ন পরিবেশে অ্যাপ্লিকেশনগুলোকে সহজে পরিচালনা করতে সাহায্য করে।

## Usage
ডকার কমান্ডের মৌলিক সিনট্যাক্স হলো:

```bash
docker [options] [arguments]
```

## Common Options
- `run`: একটি নতুন কনটেইনার তৈরি এবং চালানোর জন্য।
- `ps`: চলমান কনটেইনারের তালিকা দেখানোর জন্য।
- `stop`: একটি চলমান কনটেইনার বন্ধ করার জন্য।
- `rm`: একটি কনটেইনার মুছে ফেলার জন্য।
- `images`: উপলব্ধ ইমেজের তালিকা দেখানোর জন্য।

## Common Examples
নিচে কিছু সাধারণ উদাহরণ দেওয়া হলো:

### নতুন কনটেইনার চালানো
```bash
docker run hello-world
```

### চলমান কনটেইনারের তালিকা দেখা
```bash
docker ps
```

### কনটেইনার বন্ধ করা
```bash
docker stop <container_id>
```

### কনটেইনার মুছে ফেলা
```bash
docker rm <container_id>
```

### উপলব্ধ ইমেজের তালিকা দেখা
```bash
docker images
```

## Tips
- কনটেইনারের নাম এবং আইডি মনে রাখা সহজ করার জন্য কাস্টম নাম ব্যবহার করুন।
- ডকার ইমেজ তৈরি করার সময় `Dockerfile` ব্যবহার করুন, এটি পুনরায় ব্যবহারযোগ্য এবং কার্যকর।
- নিয়মিতভাবে কনটেইনার এবং ইমেজ পরিষ্কার করুন, যাতে ডিস্ক স্পেস সাশ্রয় হয়।