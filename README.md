# Git Practice
### New Azure Active Directory password brute-forcing flaw has no fix
The article is linked [here](https://arstechnica.com/information-technology/2021/09/new-azure-active-directory-password-brute-forcing-flaw-has-no-fix/).

### Thoughts
*Soojin Choi*
 
 The article introduces a security flaw in Azure’s Active Directory. A new vulnerability in the one factor password system can be exploited. Researchers at Secure Counter threat Unit (CTU) found, confirmed and reported this flaw to Microsoft but the response was that this was intended and by design. The article goes into more detail about how Azure AD Seamless SSO service, while by design, can also cause security issues. The key is in the error codes, which aren’t logged properly, that are given when authentication fails. Because they are not properly logged, they are open to brute-force attacks. This highlights the importance of design and how even error codes can be exploited to create a vulnerability to a program. This was the result of a feature that had flaws by design and doesn’t have an easy design. 

## Comments

### Andy Huang

I think this is a severe oversight considering how weak some (sensitive accounts') passwords are. This risk could be mitigated by the end user/organization setting long high-entropy random passwords and requiring the use of a password manager, so that brute force would be ineffective at generating a login session. There is still the risk of enumerating usernames, but that seems to be out of scope.
