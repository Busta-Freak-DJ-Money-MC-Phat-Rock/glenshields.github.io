---
layout: post
title:  "Start mining dabdabcoin!"
date:   2019-05-03
categories: blog
---

# What is dabdabcoin?
dabdabcoin is a new crytocurrency. It uses advanced blockchain technology along with [SHA-256](https://en.wikipedia.org/wiki/SHA-2).

# How does the dabdabcoin blockchain work?
A blockchain is a series of blocks cryptographically linked together.

Each block in any blockchain stores two things:
- its data
- the previous block's SHA-256 hash

![SHA-256](/iii/2019/05/03/sha256.png)

Here is an example of a simple blockchain:

---

## Block 1

**Data:** hello

**Previous block hash (can be any valid hash since this is the first block):** a441b15fe9a3cf56661190a0b93b9dec7d04127288cc87250967cf3b52894d11

**Full Data (Data+Previous block hash):** helloa441b15fe9a3cf56661190a0b93b9dec7d04127288cc87250967cf3b52894d11

**Hash (of Full Data) (make sure to remove any spaces when generating [online](https://emn178.github.io/online-tools/sha256.html)):** 7c5214a46690886837b36cf7232d3230ae7c8f0de6ec644f6706dac9dc7fe9a3

## Block 2

**Data:** good

**Previous block hash:** 7c5214a46690886837b36cf7232d3230ae7c8f0de6ec644f6706dac9dc7fe9a3

**Full Data:** good7c5214a46690886837b36cf7232d3230ae7c8f0de6ec644f6706dac9dc7fe9a3

**Hash:** f3dd9e062739743082bafc10d46ec0de63bcf41ddee0cc1ec19d196a1d03f9e3

## Block 3

**Data:** bye

**Previous block hash:** f3dd9e062739743082bafc10d46ec0de63bcf41ddee0cc1ec19d196a1d03f9e3

**Full Data:** byef3dd9e062739743082bafc10d46ec0de63bcf41ddee0cc1ec19d196a1d03f9e3

**Hash:** 7b4aadc36836965ea9c287d1f0e4832bcef4c3a55a2c10e6eaa8eecbe9c03ca9

## Block 4

**Data:** !

**Previous block hash:** 7b4aadc36836965ea9c287d1f0e4832bcef4c3a55a2c10e6eaa8eecbe9c03ca9

**Full Data:** !7b4aadc36836965ea9c287d1f0e4832bcef4c3a55a2c10e6eaa8eecbe9c03ca9

**Hash:** 76d2d721d3ad6670cb9afcc6ab6ac25950223236fac75ea974cfe213f1d6b0d0

---

![Blockchain](/iii/2019/05/03/blockchain.png)

An important feature of a blockchain is that if you change the data of any block, you will need to update the hashes of all the blocks following it in the blockchain. For example, if you changed block 2's data from "good" to "bad", you would have to update the hashes for blocks 2, 3, and 4.

This is because changing block 2's **Data** would change block 2's **Full Data**, which would change block 2's **hash**, which would change block 3's **Previous block hash**, which would change block 3's **Full Data**, which would change block 3's **hash**, which would change block 4's **Previous block hash** ...

# What is dabdabcoin mining?
In order for new dabdabcoins to be generated, they must be mined.

![mining](/iii/2019/05/03/mining.jpg)

Each block in the dabdabcoin blockchain stores the following data (plus the previous block hash):
- name of miner
- date
- comment (anything which the miner wants to say)
- magic word (10 lowercase letters)

Other than the **magic word**, all of the other data in a block is fixed before being mined. Mining means changing the **magic word** of a block so that the [hexadecimal](https://whatis.techtarget.com/definition/hexadecimal) **hash** of the block will begin with "dabdab" and the block can be added to the end of the blockchain.

Take the first dabdabcoin block as an example: **Peter Ye_05022019_dabdabdabdabdabdabdabdabdabdabdabdabdabdabdabdabdabdabdabdabeeee_mined using an Intel Celeron J1900_aaaactucxy**

If you generate its SHA-256 hash, you will get: **dabdabc8669952a26c6ac3f583d7ed9c088a5bea604a8037549522a180395bbd**

You can see that by changing the **magic word** to "aaaactucxy", the hash will begin with "dabdab". Mining is just trying millions of different magic words to get an SHA-256 hash that begins with "dabdab".

# How do I mine dabdabcoin?
1. [Click here](/iii/2019/05/03/dabdabminer_binaries.zip) to download the dabdabcoin miner.
2. Extract the files from the zip folder.
3. If you are using Windows, double-click **windows.bat**. If you are using Ubuntu, open a terminal and type **./dabdab_ubuntu**.

If you are using MacOS, ChromeOS, or some other non-Linux operating system, you could:
- get rid of your garbage operating system and switch to [Ubuntu](https://www.ubuntu.com/download/desktop) (highly recommended)
- and/or compile the dabdabcoin miner from [source](https://github.com/glenshields/dabdabcoin)
- and/or make your own dabdabcoin miner!
