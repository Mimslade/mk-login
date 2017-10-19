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

# Arbeta
För guds skull jobba alltid i en egen branch. Tack!
