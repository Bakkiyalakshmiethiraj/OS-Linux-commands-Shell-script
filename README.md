# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
![Screenshot 2024-03-21 112529](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/316e6f8f-437f-431f-bf66-3f07c642dbfb)

cat < file2
## OUTPUT
![Screenshot 2024-03-21 112315](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/75d17ae9-fcb7-46ca-9497-9ceea9e0e2bc)


# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot 2024-03-21 112432](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/d6bb210d-c803-40c9-b361-9c8bd081acb7)

comm file1 file2
 ## OUTPUT
![Screenshot 2024-03-21 112704](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/fd6da28b-36b0-4b7c-ae1b-da9f321a0cd6)

 
diff file1 file2
## OUTPUT

![Screenshot 2024-03-21 112747](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/ab8dfd60-e33f-4d41-9e81-38f763e2802e)

#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
![Screenshot 2024-03-21 113301](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/2df9a16b-b8c9-491a-9caa-cf7f4c8c2875)




cut -d "|" -f 1 file22
## OUTPUT
![Screenshot 2024-03-21 113530](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/a66ef34b-4acd-4cbb-87eb-3b76b4daa7a1)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot 2024-03-21 113430](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/f53a0dd9-7d3b-4dcd-a338-e56f3db21a51)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![Screenshot 2024-03-21 113850](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/55225733-5b8a-4fa1-bae0-fd17cdc24772)



grep hello newfile 
## OUTPUT
![Screenshot 2024-03-21 113948](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/48e35e52-a859-43a5-b872-4e86f3e84f4e)




grep -v hello newfile 
## OUTPUT
![Screenshot 2024-03-21 114050](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/7c124834-5fbc-4206-9c1f-a435737b08d8)



cat newfile | grep -i "hello"
## OUTPUT

![Screenshot 2024-03-21 114149](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/c7379103-cdda-40ed-9e69-bde353e34a85)



cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot 2024-03-21 114255](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/f171dc3c-ad28-4b78-8ad8-79d58f3ce0f0)



grep -R ubuntu /etc
## OUTPUT
![Screenshot 2024-03-21 114452](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/dac4c8bc-df80-4513-bb24-3d5a8b3e1880)



grep -w -n world newfile   
## OUTPUT
![Screenshot 2024-03-21 114748](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/afa44085-25fd-4ab1-873f-cff108faccd6)


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![Screenshot 2024-03-21 115341](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/5c17d654-786f-41d3-b20f-32fdf15e5d7c)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot 2024-03-21 115451](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/3588c168-94d9-4803-9313-aabf853bd894)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot 2024-03-21 115551](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/c2e0425a-9b7e-44ea-a39c-2f73293aa0d2)



egrep '(^hello)' newfile 
## OUTPUT
![Screenshot 2024-03-21 134800](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/8cda819f-1c93-4697-8a03-1e28ae83152b)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot 2024-03-21 135124](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/e514ec43-d482-423c-8e78-f88bd12ee249)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot 2024-03-21 135232](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/a704cf99-6417-4053-8584-c0f4b634a4b0)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot 2024-03-21 135339](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/bb2256e9-2c7e-469c-b76e-3497fb8688b9)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot 2024-03-21 135433](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/379d0126-32f2-4c4c-ac92-2f3d023f7d3f)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot 2024-03-21 135710](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/a69a5068-0480-4fa8-bfbb-f949087b34e2)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot 2024-03-21 135710](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/1f521f99-be90-47e9-9712-bd2a7a03ee8e)


egrep l{2} newfile
## OUTPUT
![Screenshot 2024-03-21 135844](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/13db49b8-0b2c-4620-889a-59b9c747b99e)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot 2024-03-21 140019](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/3bb03847-6ab2-4624-9b8e-02bff2ba02e9)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
![Screenshot 2024-03-21 140557](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/7c821be5-9f47-4c9e-a6aa-3c4bf154b940)



sed -n -e '$p' file23
## OUTPUT
![Screenshot 2024-03-21 142427](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/39513c0f-5c38-46a2-bccc-fe11fddd076f)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot 2024-03-21 142556](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/53da0ee2-34e0-4a9d-bf17-2de754d3bd43)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot 2024-03-21 142725](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/aae2a877-c29a-4122-b285-5bbbfa22dd89)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot 2024-03-21 142841](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/ce802bf0-9d20-4538-a6b2-bc779a68277f)



sed -n -e '1,5p' file23
## OUTPUT
![Screenshot 2024-03-26 105137](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/75e34a74-5906-4a70-a66b-0c06596ba6ff)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot 2024-03-26 104932](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/c03881df-75ff-4e12-b367-06abfc97f444)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot 2024-03-26 105219](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/78fe7991-546f-4af2-8a4f-af4df285b0df)


seq 10 
## OUTPUT
![Screenshot 2024-03-26 105248](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/1f88d015-ad20-4ede-8c6d-203bb8bbc74e)



seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot 2024-03-26 105329](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/8e13e5b4-25f2-4566-852a-72f94c85dcc9)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot 2024-03-26 105416](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/4627d8f2-929f-4c2f-b4b7-bd1584e1880a)



seq 3 | sed '2a hello'
## OUTPUT
![Screenshot 2024-03-26 105542](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/c557c018-9f28-43a5-91c0-7db6f37f0849)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot 2024-03-26 105617](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/a986fa94-0123-4c5c-888e-fbd146eba025)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot 2024-03-26 105652](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/00376dce-6964-4446-b432-ebc5e8dc1363)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![Screenshot 2024-03-26 105746](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/ba9f77d7-d0dc-43ed-bea2-b331fa0d2368)


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![Screenshot 2024-03-26 110024](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/89ed007c-5983-4b32-915b-c5d8bc198489)


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
![Screenshot 2024-03-26 110217](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/cbb8e47d-4fc5-4641-83b2-8dabebb5f9b8)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot 2024-03-26 110328](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/c2a2e2b4-459f-4559-b0f0-582d81833046)

# RESULT:
The Commands are executed successfully.
