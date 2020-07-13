# Image-Steganography-using-Python

## What is Steganography?

Steganography is the process of hiding a secret message within a larger one in such a way that someone can not know the presence or contents of the hidden message. The purpose of **Steganography** is to maintain secret communication between two parties. Unlike **cryptography**, which conceals the contents of a secret message, steganography conceals the very fact that a message is communicated. Although steganography differs from cryptography, there are many analogies between the two, and some authors classify steganography as a form of cryptography since hidden communication is a type of secret message.

## Advantages of Steganography over Cryptography

The advantage of using steganography over cryptography alone is that the intended secret message does not attract attention to itself as an object of scrutiny. Plainly visible encrypted messages, no matter how unbreakable they are, arouse interest and may in themselves be incriminating in countries in which encryption is illegal.

## Least Significant BIt Steganography

We can describe a digital image as a finite set of digital values, called pixels. Pixels are the smallest individual element of an image, holding values that represent the brightness of a given color at any specific point. So we can think of an image as a matrix (or a two-dimensional array) of pixels which contains a fixed number of rows and columns.

Least Significant Bit (LSB) is a technique in which the last bit of each pixel is modified and replaced with the secret message’s data bit.

## How it works
LSB steganography works by encoding a secret message into the least-significant bit of each pixel in an image. In order to do this we need to do several things.

1. Use PIL to get details about the carrier image including file type, format details, and image size.

2. Read a payload message or file and and add buffers and any other details required to reconstruct the message later. Optionally you could also encrypt the payload message before hiding.

3. Determine if the carrier image is large enough to hide the payload message.

4. Convert the payload and buffers into binary data.

5. If the carrier image is large enough, iterate over all pixels in the carrier image and the payload message and alter the least-significant bit in each pixel to be the corresponding bit from the message. Record these new pixel values as a new image.

6. If the alterations are successful, save the new image.


## Limitations

Might not work as expected with JPEG images because JPEG uses lossy compression which means that the pixels are modified to compress the image and reduce the quality, therefore data loss happens.
