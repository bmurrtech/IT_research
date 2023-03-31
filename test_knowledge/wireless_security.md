__Question 1 What are some weaknesses of the WEP scheme? Select all that apply.__

_Its poor key generation methods_

_Its small IV pool size_

_Its use of the RC4 stream cipher_

The RC4 stream cipher had a number of design flaws and weaknesses. WEP also used a small IV value, causing frequent IV reuse. Lastly, the way that the encryption keys were generated was insecure.

Its use of ASCII characters for passphrases 


__Question 2 What symmetric encryption algorithm does WPA2 use?__

DSA

DES 

RSA

_AES_

WPA2 uses CCMP. This utilizes AES in counter mode, which turns a block cipher into a stream cipher.

__Question 3 How can you reduce the likelihood of WPS brute-force attacks? Check all that apply.__

_Disable WPS._

Correct
Ideally, you should disable WPS entirely if you can. If you need to use it, then you should use a lockout period to block connection attempts after a number of incorrect ones.

_Implement lockout periods for incorrect attempts._

Use a very long and complex passphrase. 

Update firewall rules.

__Question 4 Select the most secure WiFi security configuration from below:__

WPA personal 

WPA enterprise

WPA2 personal 

WEP 128 bit 

_WPA2 enterprise_


__Question 5 What process authenticates clients to a network?__

_Four-way handshake_

TKIP

WPA2

HMAC-SHA1

This process is called the Four-Way Handshake, since it's made up of four exchanges of data between the client and AP. It's designed to allow an AP to confirm that the client has the correct pairwise master key, or pre-shared key in a WPA-PSK setup without disclosing the PMK. 
