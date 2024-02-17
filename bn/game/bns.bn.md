{
  "date" : "2021-10-20",
  "keywords" : [ "bns file", "bns file format", "what is a bns file", "file", "bns example", "Portal Bonus Map Script file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"অরটাল বোনাস ম্যাপ স্ক্রিপ্ট বিএনএস ফাইল ফরম্যাট এবং এপিআই সম্পর্কে জানুন যা বিএনএস ফাইল তৈরি এবং খুলতে পারে।",
  "title" : "BNS - পোর্টাল বোনাস ম্যাপ স্ক্রিপ্ট ফাইল",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## একটি BNS ফাইল কি?

.bns এক্সটেনশন সহ একটি ফাইল হল একটি গেম স্ক্রিপ্ট ফাইল যা পোর্টাল ম্যাপ ধাঁধা সমাধানকারী গেম দিয়ে তৈরি করা হয়েছে যা ভালভ দ্বারা তৈরি করা হয়েছিল। এটিতে একটি পোর্টাল মানচিত্র সম্পর্কে তথ্য সংজ্ঞায়িত করার জন্য পাঠ্য স্ক্রিপ্ট রয়েছে যা .bsp ফাইল হিসাবে সংরক্ষণ করা হয়। BNS ফাইলগুলি এই প্রকৃত মানচিত্র ফাইলের রেফারেন্স হিসাবে ব্যবহার করা হয় এবং এতে চ্যালেঞ্জগুলির একটি তালিকা রয়েছে যা সম্পূর্ণ করতে হবে। এছাড়াও, এতে মানচিত্রের নাম, মানচিত্র সম্পর্কে মন্তব্য এবং থাম্বনেইল চিত্র ফাইলের উল্লেখ রয়েছে। নোটপ্যাড++, টেক্সটএডিট এবং নোটপ্যাডের মতো যেকোনো টেক্সট এডিটরে একটি BNS ফাইল খোলা যেতে পারে।

## BNS ফাইল ফরম্যাট

BNS ফাইলগুলি সাধারণ পাঠ্য ফাইল হিসাবে সংরক্ষণ করা হয় যা মানুষের পাঠযোগ্য। এগুলি টেক্সট এডিটরগুলিতে খোলা এবং পাশাপাশি সম্পাদনা করা যেতে পারে। যাইহোক, স্ক্রিপ্টে কোনো ত্রুটি এড়াতে এগুলি সাবধানে সম্পাদনা করা উচিত।

## BNS ফাইল ফরম্যাটের উদাহরণ

নোটপ্যাড++ এর মতো টেক্সট এডিটরে খোলা হলে একটি BNS ফাইল নিচের মতো দেখতে পারে।

```
"#Bonus_Map_Challenges"
{
	"map"		"testchmb_a_08"
	"chapter"	"chapter5.cfg"	[$X360]
	"image"		"bonusmaps/testchmb_a_08_challenges"
	"comment"	"#Bonus_Map_ChallengesComment"
	"lock"		"0"

	"challenges"
	{
		"#Bonus_Map_ChallengePortals"
		{
			"comment"	"#Bonus_Map_LeastPortalsComment"

			"bronze"	"9"
			"silver"	"5"
			"gold"		"4"
		}
		"#Bonus_Map_ChallengeSteps"
		{
			"comment"	"#Bonus_Map_LeastStepsComment"

			"bronze"	"30"
			"silver"	"20"
			"gold"		"10"
		}
		"#Bonus_Map_ChallengeTime"
		{
			"comment"	"#Bonus_Map_LeastTimeComment"

			"bronze"	"40"
			"silver"	"30"
			"gold"		"19"
		}
	}
}
```

## একটি BNS ফাইলের অংশ

উপরের উদাহরণে,

 * `#বোনাস_ম্যাপ_চ্যালেঞ্জেস` - মানচিত্রের নাম উপস্থাপন করে।
 * `ম্যাপ` - গেমের মানচিত্র ফোল্ডারে রাখা মানচিত্রের নাম উপস্থাপন করে
 * `অধ্যায়` - মানচিত্রটি অধ্যায়টির প্রতিনিধিত্ব করে। সমস্ত অধ্যায়ের ফাইলগুলি ভিপিকে ফাইলে অবস্থান করে মানচিত্রটির নাম বিন্যাসে যুক্ত করে `map your_map_name`
 * `ইমেজ` - এতে মানচিত্রের থাম্বনেইল রয়েছে এবং রুট পাথ steam\steamapps\common\portal\portal\materials\VGUI-এ সংরক্ষিত আছে।
 * `মন্তব্য` - তৈরি করা মানচিত্র সম্পর্কে বর্ণনামূলক পাঠ্য।

## তথ্যসূত্র

 * [পোর্টাল চ্যালেঞ্জ স্ক্রিপ্ট](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

