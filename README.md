# CRC
Code for Cyclic redundancy Check in Java.
CRC or Cyclic Redundancy Check is a method of detecting accidental changes/errors in communication channel. 
CRC uses Generator Polynomial which is available on both sender and receiver side. An example generator polynomial is of the form like x<sup>3</sup> + x + 1. 

This generator polynomial represents key 1011. Another example is x<sup>2</sup> + 1 that represents key 101. 

n : Number of bits in data to be sent from sender side. 
k : Number of bits in the key obtained from generator polynomial.

<u><b>Sender Side (Generation of Encoded Data from Data and Generator Polynomial (or Key)):</b></u>   
The binary data is first augmented by adding k-1 zeros in the end of the data Use modulo-2 binary division to divide binary data by the key and store remainder of division. Append the remainder at the end of the data to form the encoded data and send the same .  

<u><b>Receiver Side (Check if there are errors introduced in transmission):</b></u>
Perform modulo-2 division again and if remainder is 0, then there are no errors.  In this article we will focus only on finding the remainder i.e. check word and the code word.
