# Cyptography: 
* basically is the art of encrypting information for computers
### Cryptography, at its most fundamental level, requires two steps: encryption and decryption.
 * The encryption process uses a cipher in order to encrypt plaintext and turn it into ciphertext. 
 * Decryption, on the other hand, applies that same cipher to turn the ciphertext back into plaintext.

# example of with ceasars cipher 
* shifting 3 letters 
### [a,b,c,d,e,f]
* a = d
* b = e
* c = f
* d = g
* e = h
* f = i 
## so if we apply this to a msg "hello"
* we get "khoor" 
* lets break it down h = k, e = o, both ls = o, o = r thats what it looks like if we shift three letters 
# Polymorphism: 
* is basically a cipher that changes itself with each use. Meaning that each time it is used, it produces a different set of results. So, if you encrypted the exact same set of data twice, each new encryption would be different from the previous one. so khoor could eqaul gdkkn and the next time it was run it would be somthing different

# 4 types of cyptogrpahy 
## hashing 
* Hashing is a type of cryptography that changes a message into an unreadable string of text for the purpose of verifying the message’s contents, not hiding the message itself. commonly used for the transmission of software and large files where publishers offer them to be downloaded 
## Symmetric Cryptography
* Symmetric Cryptography, likely the most traditional form of cryptography, is also the system with which you are probably most familiar. This type of cryptography uses a single key to encrypt a message and then decrypt that message upon delivery. 

## Asymmetric Cryptography
* Asymmetric cryptography (as the name suggests) uses two different keys for encryption and decryption, as opposed to the single key used in symmetric cryptography. the first key is used to encrypt messages and the second is a private key used to dekyrpt the messages 

## Key Exchange Algorithms
* Unlike other forms of encryption, you are not sharing information during the key exchange. The end goal is to create an encryption key with another party that can later be used with the aforementioned forms of cryptography.

#  4 Types of Cryptographic Functions
## authentication
* When we use the right cryptographic system, we can establish the identity of a remote user or system quite easily. The go-to example of this is the SSL certificate of a web server which provides proof to the user that they are connected to the right server.  

## Nonrepudiation
* One of the big problems that e-commerce pioneers faced was the pervasive nature of users who would refute transactions once they had already occurred. Cryptographic tools were created to ensure that each unique user had indeed made a transaction request that would be irrefutable at a later time.For example, let’s say that a customer at your local bank requests a money transfer to be paid to another account. Later in the week, they claim to have never made the request and demand the full amount be refunded to their account.

## Confidentiality
* With information leaks and a seemingly endless number of privacy scandals making the headlines, keeping your private information,, well, private is probably one of your biggest concerns. This is the exact function for which cryptographic systems were originally developed.  

## integreity 
* Another important use of cryptography is to ensure that data is not viewed or altered during transmission or storage.For example, using a cryptographic system to ensure data integrity ensures that rivaling companies cannot tamper with their competitor’s internal correspondence and sensitive data.