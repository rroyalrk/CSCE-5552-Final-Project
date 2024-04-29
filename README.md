CSCE 5552: Cybersecurity Essentials 

 Group 20 

 Hack the Box:  

https://app.hackthebox.com/challenges/

**Key Aspects of the Project:**
**Objective:** The main objective of the project is to decipher hidden messages that are buried within files. Specifically, we will concentrate on gaining access to and decrypting a database on an Android smartphone using password cracking, which may be valuable for forensic or security testing purposes.
Focus: A major area of the project's attention is locating particular files and folders that are pertinent to forensic investigations, like system databases and configuration files that hold hash and salt values.
Techniques: The project extracts salt and hash from Android system files using sophisticated extraction techniques. Hashcat is then used to efficiently crack passwords.


**Tools and Techniques:**                                                                                                                                                            **File Paths for Data Extraction:** The project entails finding and extracting pertinent system files, such as locksettings.db and password.key.
Database Access:                                                                                                                                                          Locksettings.db and other databases were opened for examination using SQLite.

**Extraction of Password Hash and Salt:**                                                                                                                              Hash and Salt The hash of the password, which is taken from the password.key file, is a SHA-1 and MD5 combination.
Salt Value:                                                                                                                                                                                 locksettings.db is the source of the salt value that is utilized during the password hashing process.
Conversion:                                                                                                                                                                                                 In order to use the salt value in the password cracking process, it was converted to hex format.
Hashcat was utilized to crack the password by utilizing salt and the extracted hash.
Result:                                                                                                                                                                                             Using Hashcat, the password was successfully cracked, granting access to backup data stored in the backup.ab file.


**Execution of the Project:**                                                                                                                                                           Data Extraction:                                                                                                                                                                                               The initial step of the project involved removing salt and hash from system files for Android, namely locksettings.db and password.key.
Cracking Password:                                                                                                                                                                                  Using salt and the extracted hash, hashcat was used to crack the password. This was a critical step in getting the encrypted data to open.

Decryption:                                                                                                                                                                                                   The flag was extracted from the database by decrypting it after the password was cracked.
Project Results:
Success:                                                                                                                                                                                              The project was able to extract salt and hash from system files, which allowed for the password to be cracked and the backup.ab file's contents to be accessed.                                                                                                                                                              
In summary, this challenge presents a useful case study for cybersecurity professionals and students, exposing the shortcomings in Android password security and emphasizing the necessity of ongoing security measure advancements to thwart such advanced cracking methods.


