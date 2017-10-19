# Hej
Detta är HTML-koden för pfSenses captive portal.
pfSense stödjer PHP kod om man känner att man av ?någon??? anledning skulle vilja ha det.

# KRAV
PFsense har att följande skit ska finns med för att funka.

```
<form method="post" action="$PORTAL_ACTION$">
   <input name="auth_user" type="text">
   <input name="auth_pass" type="password">
   <input name="auth_voucher" type="text">
   <input name="zone" type="hidden" value="$PORTAL_ZONE$">
   <input name="accept" type="submit" value="Continue">
</form>
```
auth_user och auth_pass används till för att logga in med användare och lösenord.

auth_voucher används till för att logga in men gästpass / voucher-kod

För tillfället så kommer för det mesta auth_couvher att användas.

# Filer
När filer laddas upp till pfSense så läggs en prefix till som är `captiveportal-` men om det redan har prefixet när det laddas upp så kommer prefixet inte läggas till. Så i alla filer som ska inkluderas så är namn standarden att ni alltid ska `captiveportal-` som prefix. Obsavera att detta inte gäller för följande filer:
 * favicon.ico
 * login.html (Filen som ska användas för att logga in.)
 * error.html (Filen som ska användas om man failar med att logga in.)
 * logout.html (Filen som ska användas för att visa att man har loggat ut. Vi kommer troligen inte använda oss av denna då jag inte ser något behov av en utloggningsknapp)

# Arbeta
För guds skull jobba alltid i en egen branch. Tack!
För att folk inte ska jobba på samma features så ser jag helst att man skapar en issue så att alla ser vad som jobbas på.  
