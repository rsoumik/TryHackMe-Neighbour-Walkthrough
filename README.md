# TryHackMe-Neighbour-Walkthrough
A CTF dealing with IDOR |

Room link :: https://tryhackme.com/room/neighbour

# Exploitation

1. First, We go to the login page by visiting the < IP >

<img width="956" alt="Screenshot 2022-11-27 105712" src="https://user-images.githubusercontent.com/109613277/204120746-cef1c36e-7e34-4732-a238-b97c55da8c87.png">

2. Now, as we don't have the credentials. So, We will view the page source or press CTRL+U to get the guest login credentials( use the guest account!(CTRL+U)) written below the Login button.

<img width="958" alt="2" src="https://user-images.githubusercontent.com/109613277/204120851-1a2f7568-e199-41ae-a984-82a7493e13cb.png">

3. Now, We visiting the page source and there we get the guest credentials > guest:guest 

<img width="958" alt="3" src="https://user-images.githubusercontent.com/109613277/204120942-613f57d8-e2e1-475f-b7be-3ddd22038800.png">

4.  Then, We getting back to the login page and put in the credentials.

<img width="960" alt="4" src="https://user-images.githubusercontent.com/109613277/204121057-4df8784b-6456-4e28-8be2-a7de43a0c352.png">

5. Now, We are a guest but the page says not to peep your neighbour’s profile.

<img width="960" alt="5" src="https://user-images.githubusercontent.com/109613277/204121133-b9650d62-3987-450b-a960-7a79eb7678fe.png">

6. So, What do we do now? Now, We will view the page source again.

<img width="959" alt="6" src="https://user-images.githubusercontent.com/109613277/204121268-078cdada-a06d-44eb-b757-421e0bab1f3a.png">

7. Now, here we got some hints for the admin page and we know we are still logged in as a guest.

<img width="958" alt="7" src="https://user-images.githubusercontent.com/109613277/204121356-dc3b14d5-b47c-4339-b558-8ae8f17ac202.png">

8. So, Now as we know that this challenge is IDOR. So, We try to change the ‘guest’ with ‘admin’ to login as admin.

<img width="956" alt="8" src="https://user-images.githubusercontent.com/109613277/204121428-7afbade8-c616-4670-a25d-3f0848a8379f.png">

9. Now, We are logged in as admin and we have got the flag > flag{*******************************}

<img width="960" alt="9" src="https://user-images.githubusercontent.com/109613277/204121540-9ef779e1-48bd-47bf-ace8-c9f85c162ed3.png">

10. Now, submit the flag.

Thus using IDOR vulnerability, we bypassed the authentication.

What is IDOR vulnerability ?

Insecure direct object references are common, potentially devastating vulnerabilities resulting from broken access control in web applications. IDOR bugs allow an attacker to maliciously interact with a web application by manipulating a “direct object reference,” such as a database key, query parameter, or filename.

Hope these things helped you a lot.

Thank You.




