# File System

This is the project I am most proud of—a file system created for Linux. In this project, my groupmates and I created and managed free space and directory systems and implemented directory functions (such as mkdir and cd) and I/O functions (such as read() and write()). See below for run instructions.

Several elements were necessary in creating this file system. For one, we needed a volume, a place to store our file system. We also needed a volume control block, which is a block of data that stores details about the volume, such as the size of each block, the number of free blocks, and the number of total blocks. In addition, necessary to our project was obviously a directory system. We needed a way to initialize not only the root directory but a way to initialize subsequent directories that a user may want to create. What’s more, we needed a free space management system, which is in my opinion, the most important thing in our file system. This was central to the project. Without this element, everything else we can possibly work on is moot if we don’t have a system to store, track, and manage free space. We used a bitmap in which we manipulated individual bits to keep track of space in the volume. Directory and I/O functions were also necessary as that’s how files are written into and created. There was a special function that we needed to create called “parsePath”. This function was essential to parsing/tokenizing each of the directory names in a path, traversing each one, and loading each one into memory, again and again, to allow us to perform certain directory operations on the final element of the path. Finally, we of course needed a shell to help us perform these actions for the user.

To compile and run, simply type the command “make run”:
![image](https://github.com/user-attachments/assets/afe44dc2-3c0e-41d9-8147-0d8bc555f2fb)

The user is prompted to operate the file system in almost the same way they are prompted by Linux’s file system. They will see “Prompt > “ indicating to them that they may begin operating it. Here is an example:
![image](https://github.com/user-attachments/assets/49ed0a27-6ae7-4627-9883-f6aac09ca318)
![image](https://github.com/user-attachments/assets/c2907903-997d-4f72-a52f-7608a9e6e0b8)
![image](https://github.com/user-attachments/assets/67680093-8d5f-4bc8-8282-917ae7493617)



