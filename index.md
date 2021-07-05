<h1>How To Install Jenkins On Ubuntu 20.04</h1>

<h2> Jenkins မိတ်ဆက် </h2>
<p> ယနေ့ခေတ်မှာ CI CD နဲ့ ပတ်သက်လို့ tools တွေများစွာကို release လုပ်လာကြပါတယ် ။ အဲ့ဒီ tools တွေထဲကမှ Jenkins , Gitlab CI/CD, Spinnaker, AWS CodeStar နဲ့ Travis CI တို့ဟာ အသုံးအများဆုံး tools တွေပဲဖြစ်တယ်။ ဒါကြောင့် CI CD လို့ ပြောလိုက်တာနဲ့ ကျွန်တော်တို့တွေဟာ Jenkins အကြောင်းကိုမေ့ထားလို့မရပါဘူး။ Jenkins ဟာ java-based open-source automation serverတစ်ခုဖြစ်ပြီး deb/rpm packages (သို့) Docker (သို့) Jenkins Warfile တစ်နည်းနည်းနဲ့ install လုပ်နိုင်ပါတယ်။ ဒါကြောင့်ဒီနေ့မှာ ကျွန်တော်တို့တွေ Ubuntu Server တစ်လုံးပေါ်မှာ Jenkins ကိုinstall လုပ်ပုံကိုလေ့လာလိုက်ကြရအောင်ဗျာ။
</p>

<h2> Prerequisites </h2>
<ul>
  <li> Jenkins ကို install လုပ်မယ့် server တစ်လုံးဟာ အနည်းဆုံး RAM 4GB ရှိဖို့တော့လိုပါတယ်</li>
  <li> JDK 11 ကို install လုပ်ထားပေးဖို့လည်း လိုပါတယ်</li>
</ul>

<h2> Installing Jenkins on Ubuntu </h2>
```bash
$ wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
$ sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
$ sudo apt update -y
$ sudo apt install jenkins -y
```



  
 


