# HolidayHackChallenge2021
**<p align="center">**
![image](https://user-images.githubusercontent.com/33500545/148440994-34860215-6845-493c-b5b1-a9d237360875.png)
</p>
<p align="center">
Notes from 2021 HolidayHackChallenge
</p>




# Now Hiring
You are directed to apply for a job over at https://apply.jackfrosttower.com/
So first thing is to check the site out, when you click on Opportunities you will notice that the images do not load.  There are 4 images (1.jpg, 2.jpg,3.jpg,4.jpg).
So I decided to run this through burp as the images aren’t valid it seems.

I enabled my proxy and went to apply.jackfrosttower.com/images and that resulted in a ngix error, I then sent that request to repeater, and in repeater i tried 1.jpg, with no result.  Then i tried 2.jpg and found the super secret key.
No WIN
![image](https://user-images.githubusercontent.com/33500545/148627937-e53e60be-4605-48fd-bc20-01a8a781c8cc.png)

WIN
![image](https://user-images.githubusercontent.com/33500545/148627923-aa7de3c7-2f85-4439-83f7-bc1c762baa12.png)
