# Petshop-Pro - Hacker101

Capture the Flag Lab step by step available on Hacker101

Link: [https://ctf.hacker101.com/ctf](https://ctf.hacker101.com/)

Tech Used:
* Hydra THC

<h2> Flag 1 </h2>

<p align="center">
  <img src="https://github.com/bensadel/PetshopPro-Hacker101/assets/95494769/12789958-6d6b-43bc-af7e-676ff3d1a639">
</p>
<p align="center">
  <img src="https://github.com/bensadel/PetshopPro-Hacker101/assets/95494769/3a6c46cb-ec69-4674-b427-1c4ef1427f07">
</p>
<p align="center">
  <img src="https://github.com/bensadel/PetshopPro-Hacker101/assets/95494769/036daed2-5cb3-4559-9bde-07779e832c5d">
</p>
<p align="center">
  <img src="https://github.com/bensadel/PetshopPro-Hacker101/assets/95494769/2bb1d9e0-8c7f-48a1-8cf0-385522f2de33">
</p>
<p align="center">
  <img src="https://github.com/bensadel/PetshopPro-Hacker101/assets/95494769/5ffb2661-0f3f-4e75-af8c-54a000c15f88">
</p>

I found Flag 1 by using the Google Chrome Developer Tools. I changed the price integer of the added photograph from $7.95 to a negative integer -1. After saving my changes and clicking checkout, the first flag appeared. 

<h2> Flag 2 </h2>

<p align="center">
  <img src="https://github.com/bensadel/PetshopPro-Hacker101/assets/95494769/e98a15e6-8dbc-4af6-a8cb-e767a810bbdc">
</p>
<p align="center">
  <img src="https://github.com/bensadel/PetshopPro-Hacker101/assets/95494769/cfb4c024-fdd4-4266-9db5-632176452444">
</p>
<p align="center">
  <img src="https://github.com/bensadel/PetshopPro-Hacker101/assets/95494769/476ae33d-00be-4743-ba28-db4b452e19f8">
</p>
<p align="center">
  <img src="https://github.com/bensadel/PetshopPro-Hacker101/assets/95494769/4f4af7d7-a255-4158-84cf-0b2c8ed85a74">
</p>
<p align="center">
  <img src="https://github.com/bensadel/PetshopPro-Hacker101/assets/95494769/ebe3ac04-8c81-415f-913d-31a4ad5e031a">
</p>

I found Flag 2 by trying different URL endings and using Hydra THC with various world lists. After confirming the existence of a login page, I attempted to guess usernames and passwords. With no luck, I decided to move to Hydra. The first script I ran confirmed the username was correct by ensuring the "Invalid username" message changed to "Invalid password" while using a dummy password of "test". Furthermore, after obtaining the username, I ran the following script for the password using the valid username. When using the correct credentials to log in, the second flag appeared.

<h2> Flag 3 </h2>

<p align="center">
  <img src="https://github.com/bensadel/PetshopPro-Hacker101/assets/95494769/1eb4d016-3203-48a5-8b9b-3ca4acd1fc42">
</p>
<p align="center">
  <img src="https://github.com/bensadel/PetshopPro-Hacker101/assets/95494769/6503a884-65e6-4231-abb8-ea93825f7273">
</p>
<p align="center">
  <img src="https://github.com/bensadel/PetshopPro-Hacker101/assets/95494769/2e5f1826-a34c-400c-a412-cca0565ebf65">
</p>
<p align="center">
  <img src="https://github.com/bensadel/PetshopPro-Hacker101/assets/95494769/fa073b69-eb95-44ab-b811-55031244690b">
</p>
<p align="center">
  <img src="https://github.com/bensadel/PetshopPro-Hacker101/assets/95494769/9258e98d-394e-4e00-b17b-6e48a92802c2">
</p>

I found Flag 3 by using XSS scripting. Upon finding Flag 2, I noticed I had escalated privileges compared to my Flag 1 visit. One difference I noticed is that I could edit product item descriptions and save the changes I made. I input two XSS scripts, one in the name box and one in the description box. Both scripts were <img> tags with a src attribute of x and an onerror attribute of alert(1). Since the src attribute did not contain a valid src, the onerror attribute triggered an alert after saving the changes. After adding the modified item to the cart, the third flag appeared.


