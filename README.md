<h1 align="center">Guide for BASH Scripting</h1>

<p align"center">
  <img src="https://repository-images.githubusercontent.com/560483284/d197fd68-fe5a-44a3-acd4-fdd9a026da2a">
</p>

This repository contains a walk-through guide required for you to start BASH-Scripting

# Prerequisites

To use this repository, you need the have a linux installed on your system.
>For windows users --->Use WSL (windows subsystem for linux).

 ## What is BASH?
   **The main creator of Bash is Brian Fox, who started coding it in 1988 for the GNU Project.**<br>
   To understand it,
   imagine Bash as a translator. Instead of clicking buttons and menus, you tell it what you want to do by typing simple commands. It then translates those commands into actions your computer can understand.

  Think of it like a super cool assistant:

  Need to copy a file? Tell Bash, and it'll do it in a snap.
  Want to open a website? Just ask Bash, and it'll launch your browser.
  Feeling lazy and want to rename all your cat pictures at once? Bash can write a quick script to do it for you!
  
  No fancy mouse clicks: Learning a few commands opens up a whole world of possibilities.
  Like building puzzles? Scripting with Bash is like putting little commands together to make cool things happen.
  Get things done faster: Save time by automating repetitive tasks.
# Basic Commands
pwd: `pwd` command is used to print present working directory, it returns the directory where you are present.
```
pwd
```
cd: `cd` command is used to surf through directories (directories are like folders and files)
```
cd [directory name]
```
this command will direct you into your [directory name]
For example :To move into Desktop
```
cd Desktop
```
ls: `ls` command is used to list all directories or files inside that directory
```
ls [filename]
```
For example,to see all directories in desktop 
```
ls Desktop
```
mkdir: it is used to make new directory
```
mkdir [foldername]
```
For example, you want to make a folder named "frontend.txt"
```
mkdir frontend
```
If you want to create new folder "frontend" and want to be inside this directory also ,then use `&&`
```
mkdir frontend && cd frontend
```
touch: it creates an empty file and it also use to update time-stamps.
```
touch [filename]
```
For example, you want to create a new file named name.txt 
```
touch name.txt
```
To update time-stamps use `touch -t YYYYMMHHmm.ss [filename].txt`
here, 
<br>y-year
<br> M-month
<br> H-hour
<br>m-minutes
<br>s-seconds
<br>
For example, to update time-stamp of name.txt 
```
touch -t 202402011200.00 name.txt
```
cat: to prints the contents inside the directory
```
cat [directory]
```
For example, to view content inside name.txt
```
cat name.txt
```
cp: its copy-paste, used to create a duplicate of specified files or directories in the destination location.
```
cp [options] [source] [destination]
```
For example, you want to make a copy of name.txt to a self made folder frontend
```
cd Desktop
cp name frontend
```
(for copying file ,we don't need any option, but for moving folder we need `-r` as a option)<br>
>Q) What if [destination] is not made previously?<br> Ans: It will create it itself on your present directory
<br>
mv: It is used to move directories from one location to another location.<br>

>Q) Can you rename a directory using `mv`?<br> Ans) ofcourse! By moving a directory into itself it's name will be over-written ,thus renamed
<br>

```
mv [options] [source] [destination]

```
For example, you want to move file named "name" to a new folder named "new".
```
mkdir new
mv name new
```
***If you are not giving options ,it doesn't mean command will not work, it's just it will work without handling them properly or avoid special handling.***
## Vim
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAMwAAADACAMAAAB/Pny7AAABBVBMVEXMzMz///8BmDMAAACAgIAAXQTQ0NCzs7Px8fEBfRfe3t5eXl5F/gF0dHQBmzS6urrBwcGtra1m/pgBoTY4ODhBQUEsLCyHh4cjIyPo6OgAHQqfn59YWFgAOBNJSUkBhi2Tk5NqamoWFhYODg4AWR4ACAIAIgscHBwAkzQAEwYAFwhQUFAAVgAAPhUAQxYAYwQAUQRA7AE4r1MBeikBYSErzCImnwQASxkBbRIBhhkAOgIAQgNG+yIBbSVZ3YQlXjhE0nBf7Y4dtCoALxA94QEAMAEAJQUjoCQsbUEplQFDpmQPBRA9wGQWqi0XhQE3zwkZcQIlwCUZPyZOwnQRLBoeTC0ibDRVJfqVAAAUwElEQVR4nN2da3sax5KABxoNeCQGMIgBgdAgxFVSJK8cS5at+Hh1rE02OU5ydrP//6dsV1+r5wJzRc859SHOI2B63unq6uqq6h6rsg9xpntpxtpHIzYh0320sw8Ya0lOSLOxh4b20ESP/Pxfa1Irn6Z8mPYx+fnr5w+bX8unKR2Gsbz9fLQPmrJhOAuF2QdNyTDtHmMBGEpDauW2FgXj5JehuHqfszCYow/rkmkiYDr9/DIYwZXsGfnCWDjM0S9z0gw0Zo97+WVsx8G0BqQIoTQOIV/evkUwR7+QAI3dK6SxiR0N0+4XcnlKY2uWv3WPjqL6xiqoLUEThLEn9KPlcV7hvatYPq7+caT6phZgWQ5yClzk0g7DOGO4emeYV0asha+CpVqtrv4hNW3+qycsdJ2x9EedfFKvzQSNCTNsMpbQOEovjOa/FQul+c93gmYtaRhLr56/MX8JNI0AjE3/2geWfIaZ3msDaOZfFQui+bD+1QeaoWRp5GqsAo2BHRkGYejo9+HfVjuXDNl0SU6+apYwDcDMqNFrWK12K6u0W214LtMYmDqwWLmk3bY6Xp/BaBag4ePmM6XxOMyyRVnadh6hj641OoyBoVrWsfPB2G2/VmMwmAVojhANg6lXnHbexrxabVw+zOa3qinaQs+JV+EwOdui0qx5e+iZ9coN0qjZk/oC/+owmuY7nzD/pWG0pn3/N4DRvsD3fwMYZaHfFQNjt18TRtIUA2Nbo1q5MHVvG4ygeVfEPENZmtthnDqeYhNeFUmLsmyD4TQChvobqRvDLLSpmhc3aYIX6yAPu52oARs78sCyFYb5AgAzaEGr9ZGUlDohWGrTQRQM/WMP/FD+HZBOKxlM06sZMqGLjHksDNAADHNrK774TTNhY6pRm99nE5YAIRgH1pmDYaXRFJefthv1hDABFrj8fTeOhc03V+A2U//ZkSyjRrrxI1lgcUas0EqTBxgqjri1qV1p1JNdl//C48JZ5ltYGM0jfKtW8fmPKEsllbtud/hdMhZYCUTGAIg/ZXJJ1yWpYLxDHvvhIYBYHZM07xhNn//mHOKdaWDsDn+ARLKEozPWBAU9GmlhLvVv52c7YOi4+fuj/n4TAodpYOpN1S8zvvYOx80wTXqYmWJ52sVCaf78/dFgSQPDWdjYn4moRUREs82HSz8rzPxlQeViJwrQ/Pjn7eOnNbA4vO2kKHadtdfsi7V3HAyX4WFWmM0dSLxVNuTP33//vlEslaSmmbPUmsxeSZZ4GCczzEnXpZIIBfrmx1upY7TRhDAGi46MlQKTEATEvXshZKpYErUVx/LaMO7dCSGHqVm4t2Hq2KvDdO82BbK8Lox7N8/AwnzymsdYfCOx+Jow7hlBLMna2cbymjCMRY79YTJ/divLK8J0GYuTkqXNx8sxsHjB5HXBMOAKJYPhOqZYEjWiWJgLGE7EvxaMe5eHZRbJ8low7t06C4uvWaTT8PowbK4cC5bENlmynMewvA6Me7cg5FKyJPSUJct4hozg68O4T6hfhmlZztHk9PowbLxkZPEOZ8hwvD4Ms2MTyZJ0vIhgH9yUUtDXh2Esl8qOJesYHoQVLOM4lr3DMBZ5O416snCphVku7bhb3jcMZxG302ilY5nuYNkzTDYWm7HUpmDHJtuq/fYK4z6t9aNNztLh/QJBpd7WysU9wrhVmF8mkqWdML0gWSBK2t9ehbnPngGWYzn2E7OgpMVsR0XpHmEYi+6XRJeVwXHO0t7Osj8Y92mTnYUHYXdW+u4Lpvs0z8HCIti7+mVvMF2wyb2UY18G+3jSorWTZU8w3SeS3o4ZLLMELPuB4b6llZHlnAViErDsA8Z1nwyWpMHxFh8vYMfm836SUs7yYehcOc/BAgmYzS/fSRKa0mEoC9hk2U5aFhbs+3D07o8kNGXDcB+mL8e+lY3lKBlNyTCCReqYlXTs8yCsZklGU3bPgI4hlkTXkiw8aXHxJy9Pe3fDi1NeDYb5/MrVzcZSXQmaz1ekv52mVBg2V2qWxME+FOi/oJoqaY4+7aApE8ZksdMF+r2+ZKlqmpftNCXCdN/jpWFyFt/slyqmedxKUzDMsYJxXcYiXd0ULOxKLAFzr4oJVj8KmlvSi6eJhWkf54Jxq4xFNpyWZWKyUBE07w620MTBWCyfkxmGsoAdS81iYZYqYlkpmpt4mhgYUQ2UFcZdvafzyyC1jvEAGU9a3JsFK4rm73/E0kTDUJZ//pUdhveLZknqw4iKS8ZyHSy+0TSxfRMJYx+TL//zc46eCbAkuoJmgUXyD1GFRHrcRNu0KBi7R/76+tOXrDCLLrAss7KMY1mUTXt3S/pREYEIGNov//v1bXaYzft5dhaPsZzGVBFKms+ftNHfCkNZyNu3OWDInG2/4pI0+WrhBEwcC5pvXqJoQjCCJQ8M0e5t0mIFGVDewWLQhDUtCGNRHXubF0YNz2HSCnKTZVuCR9FEaFoABmzy1xwwbHpSi6iULDWWsHzeylLVNu02RGPC0Hn/L7GH97frrD0zyMxynoRlhSz0cTsexr4kX34S+5HPTjPCnCuWxOOFV/Wy4PjibmcVAZ49TRoMYyEWNyvMTLIkLR6VwT7GstnNgmkCfYNg6NhXLNVqNpge0SzJUGSFMmNZJ2HBNFcGjYaBeV+zZO0ZxZK03Npmu20kS/IKYkFzizOD6v9ov/wT7d/PBtOUjylpsYKsHmUJmHliFuTZPOoAo4KhLPO3miUjjD9MyyICZLOULFVloT+faBrxr5z31f79TDDNlrRjiVl4oJ9NtQl2QkTRHOngryX7ZWOwZIPxePa1kXh+QSzzpzSF6gbNixw37L963lf797PANDuNLCxMx9bpWZRN+yzHjcVZ/gqwZOsZKx1LW4/99fvULJTG/V15NixlYnEf5qcASyaYETsZIy0LC/ZlYUE0dL6ZsA10tF++hFgywbRTjf02CvRnYwnRWNEsWWB8J41N5oHLfCyY5obSWD6Z/99v/8EEfysDzCh5kSId+5glpU025QOXgznxreGUbK7e/EHlzcdcMJ6VgkVUj3KWanYYd/Vwy+RxTqZDC85s2Ry8YYJo0sP46Vn6BbAcgNzcrqE62GIn0KwfgjTpYdoJv6kD/QWyzFmlM5hnOE8nSJMeJrkdE4EYlIDJx3JwK6q22TwXQZMaxk++X5RXXPbyslRXD1cGi/DNwjTpYRJvfufB8V4o0J+HxcFesxOkSQuTVGSgP5y0SCluNcSi1jNBmpJgTJaEu2y3sbCxL6u21SoNbBqy0OXAKJZZ7n65u5I2We8M0AtoSnOiaUqAsR3H7tTY0QfFsWxwNT2Kzhg0hcMwg9y8BDmOT1rkYjHiZg6iKRrGtqivPyNKcrIcRLGYEU1Ks5FWoFgY2x4jkogkXwaWgyBL8HSTQzIXNA/PhcLAtNI7ZDKGqX/nmRQJWNZqG04kDJo9H74VCGPDBoupJc5XbB3D1J9Z7tT8EtwVFMzPKJqHlwJhHHqtpj67qJk+rhRiuYrYFRTKnEGZyUPBamZ3CDlWcXS71cuhZogltJMmnNMUNEXCwCUPHYU2ymEAhE2+mkewRGWbadPrh49Fqpk9I8uRdkRrsIrJxULtWNQOp6g6AGdMTh4KNACOPyM9S2lZmzpm6cLKQlxXspyo8vWdMEDzclsYjA3Wa6q1rAW5vgwwmmWhtkgkgAGazaYgGLtVW5IZCg362fxlynIgWSL7JbaqiZ3bXAiM3YITD/qO/sMkU3AJs0T3S3y9GafJD0NZeNbWEefkwcLpJMOQESwHVyexLPGVgOxssNwwLAgLexL7ns9lyrz/DCx8fjnYqG04KWBS1mhuYRGFF8hjzrCSkSzz+H4pGQYnLYpi2bbrtEwYycISyddSskSXpA+z3s8O2igWy8cJGCVZWW6uFiizvF8YUdWbJ5nEBc2V23cDlwdTUAJG98vty67dwKXBSB3Ln4CRc+XLrn4pDQZYIKgELPOnbjc0YtxuQAxe9Ombg6T9UhYMxJWavX6fv2Tk+RQJdzG7Z+8vTMFOQffu/gch18+fbsCOiSrGoY9lRyVgMTAsRhbzMha+U+DslMwDonWxC0frKZl/ozQLzuKczwwJ7Nsqp2dGTV4+FiWrqtiNEhQZFnDPns0PPh2ccJZG6DemN1AKDGWB+uTzjm/K6HBG1syw3RMyOcTSYzRMWMSuJoRXSvOqMmBZjo3fHG+JmxUDw862ZguywJsiwBW/6IojGm3j9R6w/CR3Kypn93DMp3KyW+yg4lFjOGzQSw589Jv6IHDGWfEwvHoUbLIHb+5AJ8vYdfpHWJbBPqEee62HWrLZ7KZPFovFCX38vg5LsR9JmfkObsk/NzejFw4jKmHZ8xwsl8uBjmTY3oxsmJZd0Bum0kfpNrt+LG/5vGahNJzT0aOv5hhNWVBDVCKMZJnJ9i9R3emh9AUu+Gc9XF9rdy7FYcdNc2uqM5oIaQZSjRApGZQHI45WYLtGnp+f5/Rh6o7pCC2j9ur++XQOYTzjt/WYU9XtOpeOFfygae6tLxZGsPBk0tnZGbyRCWkZBeTm112dnW3IuWfeXOwR9DF/t1uXhMSmNPLCcBaPs6xcOGti3NbxsikKMXfv1mSQ9HSjuOZGS9Ivy5qJCmUWCoFkUvcUwuWatC+0jMHATONsu1qC9rzyTDOvUuQsLJbsmlrmA6J0WVZ0lle2LPzuInTV2M/s1mHgyJPiYDALcyfBZ7lEUdlDpGXsJD2dFvACroKvJifbb5pS09kEarNn5XgAdquJWMAAdxdk1tRRWZguzrCWjeVnIuKIZCJHEwvtGnKpB6EfPEyzsO3A/GR0vANmBe9MC0RllZadwssDJUzIf/R1xwT9VfV4mEExNwUWBCNZlpqlewFHzegv0Mf/pJx8Q8tG1JW8F/LtG7j/6hlA/nAsX2zh1fDjsVt9sizDaxYVypil6r6Qmae1rE7IQmmZe4GyT9DSD2Jdubq5uUVeQ2AmsaC4HD+DwNGghcCIin6+m0ey3NFZsW1o2YXUMvfsGj/9viw3d8/oovKRjgR14REd4/qepjg1Yk0D52gXA4NZXuQOGHMisWGzNLJlFFR91FmSjfByYLm/pgsAxVnDbxNtDFACzm4P9Cbd4mB4JSw/5m4hl/KuMZGwDNOLXuZTLZuq4U+f8GlXsVAtm9SVlhkzSZtO+GgO1qVZxcHwAJnXNFiou7LQQ5xP1vday061ltmQbgAt4yygZU31K6pl53pYNJE5Z5nR4AFOuWEkC9jkjX72zJahDNMARQLhHKq+mkmYl6NYDjZ0BYZnEv2O9MYEmXO44jJ4Dk1eGB7s8+DVeGStKxXc1bXRspnHfI+evlObkeeuYjmgBkt1WtvUsj7u63aSooZ0MPxoBY/tgNmgXSNdOHAGdUwTvSaIRV/0bDpmfXbG4/w39KNDaX3tuuGv1KC+RF2xRsIvgc4HI1jYeMEsbCKZ6sfo4A0yoGWqXoOt2CifYPlG1/lqbWz6K41D3NdOX7/cpBgYUaXIEjAmCx7ifMZEWnaBZxL6hF+6guUA0vU9rWVTQvSwgFenIoeCRKSc88BIFhaENXYmuU9zMtBfBOv7g+qY1Qt+xLBiWyEW7Wgzf0Xfn2/MW9Q6TkP3nAPGYLk182EXePFv2cuAlk20llGvWOaRv5GB4Uka/kqjiect55gavQJhJAuvHP/4BtUpBIa43ZmRxQprmZ5J6PM+USxkNMPLOcNfsSi19v6tyGNoM8OIin7RL1Chpm+XDXHtl3FPUqGuybm+Yfq8H5WOdVoz0tM3fI79lQ4cxYefwSR8z1lh5PEdmgXRrOjD99BXe2jjIoBqrxgif7eSZVQ5RJ4k81e0lsF6Xz+eywjDnKNn0E4L8vxG0EgtOzG0bLQkc+0a3KMoBwyLxZViqfSwkznF/opNb18vmC3DNOSFEcdEsGXg+Ji8GDTw8MctQ8uulZa5EP1Wn9W4lt1wFuoIL/UzIPjcvBZomX4G1OWMuOdsMJjFr1ATuvmIaFb3hpbBMl4vywwtg2j5LWeBTsCeJGiZPv6/4eNLssrComAEC9MxUF2TxqWL/wHSMljG68PorgPD4uTq4OaRszTGgQWzp++GUqPA9HH0sbpZYERwvCdZGI3WNDjQdIqSFVP8+sauEUtjWgYs7LaNOd6BJ6Lupo0iNlTL+kbwPw+MOPLiWLMwGmkFqu4zNjx2fQJaJl581sVG24Yz1D4dPMqBjud48LPHeikzQh6Q5VB1vCwGhgfI+A4YbR4pzTdRq36G/CuREXp6/ySyzIaWUZdt/fg4l+qE53h2w7akGV5iDwgc7WnLaoTueTdMYK+yOL6DsTTR91s9SXOLvHiLzeMgbCeDu1rjOlpPRMnErdB+Ur9zwLgsa4LGRmtp7mgT421tO2HGAsY4kdjGLGY4UdJ8pGtFpGWiZb6ihvO0+/pqfJbqiQuMUJwNTAOIsM0d5AExRxtkmhymQf0k1v+NdqutBSVggu9/AhooVTe1rO7VPFiIsiWAoWXUl/Fqeipv1HAo3b8cjxUMLJhRxpDO12Ahm5WgxJdwgGlnDTnitaogvqcSMLXQO2AYzcdPkBELZJmpPp0yLVuQWUuni20HFsZiWQKBDZ2Btpl3IBbGDvjZDv6dPcO2bjcMsy5A0w68K5cfyBT1niGwaR+pHznt4Bcfdzp16pxBOIOd4nY41nI4OSdLcSGqSrMx/qynRhP9aHCJPxvTDp2kMAAgHhsYnik+O8cx+j1DdNG+oB/Ozk1ZioLZ7gUJixx5nfBH8mCpWsTPUjmaTKBvlj1T2KiNec8Q0ETLMw/zLcKfyMWvFUxe6PsNpwnYC5lTwjCaCIlj4TTrxQmThZYXvjxwz96/v3jkQj3r6Wg00lcadkam6HzFcBSSsJLthKn45xEs8e/mYTSPbz6CvHHD5WRu173h8mkepSj5ZGdBWqcWli0sjOabub7BkY7VAQ9elMGyGya9dPq0b6Jp3NWNYFmXwFIGTKVOaR6iaNQGfsri7b5OaikDhtFE9A1mCceJCpBSYIDmOkRTOktJMJVO2AqoAy9K0rFKaTCVzpJ6NmK1FmCZo5xLsVIWDPTNixHluBEsUe5uQfL/UZcVyMSdHFkAAAAASUVORK5CYII=">
<h6>What is Vim ?</h6>
Vim is a Unix text editor that's included in Linux, BSD, and macOS. It's known for being fast and efficient, in part because it's a small application that can run in a terminal, but mostly because it can be controlled entirely with the keyboard with no need for menus or a mouse. 
<br>
Vim is also commonly referred to as Vi because when it was written by Bill Joy in the late 1970s, it was short for visual editor. 
<h6>Some Basic Vim commands</h6>
vim: `vim` command is used to open file in vim editor

<br>

```
vim [filename]

```
For example, to open file named name.

<br>

```
vim name

```
Press `i` to enter insesrt mode in vim and can make changes.There are several modes in vim like Normal modes, Visual modes, Command-line mode,Ex mode.

<br>
After writing, you can exit vim, using `ESC` + `:` ,then type 
<br>
<b>  q to exit without saving</b><br>
<b>  wq to exit with saving</b>
<br> 
<b> "!" before w and wq to imply forceful action ,like !wq and q.</b>





**For vim cheat-sheet ,<a href="https://opensource.com/downloads/cheat-sheet-vim">click here</a>**











  
  
    
 
