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
<p> Jenkins ကို install လုပ်ပြီးသွားရင် service active ဖြစ် မဖြစ် သိရအောင် systemctl နဲ့တစ်ချက်လောက် စစ်ကြည့်ရအောင်</p>

```bash
$ sudo systemctl status jenkins.service
● jenkins.service - LSB: Start Jenkins at boot time
     Loaded: loaded (/etc/init.d/jenkins; generated)
     Active: active (exited) since Mon 2021-07-05 23:32:59 +0630; 8s ago
       Docs: man:systemd-sysv-generator(8)
    Process: 1188529 ExecStart=/etc/init.d/jenkins start (code=exited, status=0/SUCCESS)

ဇူ 05 23:32:58 thaunghtikeoo systemd[1]: Starting LSB: Start Jenkins at boot time...
ဇူ 05 23:32:58 thaunghtikeoo jenkins[1188529]: Correct java version found
ဇူ 05 23:32:58 thaunghtikeoo jenkins[1188529]:  * Starting Jenkins Automation Server jenkins
ဇူ 05 23:32:58 thaunghtikeoo su[1188568]: (to jenkins) root on none
ဇူ 05 23:32:58 thaunghtikeoo su[1188568]: pam_unix(su-l:session): session opened for user jenkins by (uid=0)
ဇူ 05 23:32:58 thaunghtikeoo su[1188568]: pam_unix(su-l:session): session closed for user jenkins
ဇူ 05 23:32:59 thaunghtikeoo jenkins[1188529]:    ...done.
ဇူ 05 23:32:59 thaunghtikeoo systemd[1]: Started LSB: Start Jenkins at boot time.
```
<p> Jenkins service က active ဖြစ်နေပြီဆိုတော့ jenkins ဟာ localhost ရဲ့ port 8080 မှာ run နေပြီဖြစ်ပါတယ်။ port number 8080 ကို defautl အနေနဲ့သုံးပါတယ်။ ကျွန်တော်တို့ အနေနဲ့ Jenkins portကို ပြောင်းချင်ရင်တော့ /etc/default/jenkins မှာ HTTP_PORT variable ကို မိမိ ပြောင်းမယ့် port ကို ပေးရမှာဖြစ်ပါတယ်။ </p>

<p> ဒီ tutorial မှာတော့ default port 8080ကိုပဲအသုံးပြုပါမယ်။ ဒါကြောင့် မိမိကြိုက်နှစ်သက်ရာ browser ကိုသွားပြီး localhost:8080 ကိုခေါ်လိုက်ပါ။ ဒါဆိုရင် အောက်ပါပုံအတိုင်း Unlock Jenkins Screen ကို တွေ့ရမှာပဲဖြစ်ပါတယ်။</p>
![Unlock Jenkins](https://github.com/thaunggyee/jenkins/blob/gh-pages/Screenshot%20from%202021-07-06%2000-02-09.png)

<p> </p>



  
 


