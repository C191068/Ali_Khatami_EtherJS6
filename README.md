# Ali_Khatami_EtherJs6(Learning from the video of Patrick Collins)

### Interacting with Contracts in Ethersjs

Now we have deployed the contract at https://github.com/C191068/Ali_Khatami_Ether.js5.git <br>

We can alos learn to interact with our contract through code as well <br>

![d15](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/3183fd46-1806-4d7b-ba67-636c76706a75)

Here we use the above line of code to retrieve current favorite  number <br>

the contract object thet we have is what return from our contractfactory  <br>
as long as we awited it <br>

the contract object can come with all the functionality in our ABI <br>


![d16](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/d196f994-12ea-4f54-af6c-5dc8be8ffe92)


that is why we have to pass ABI to our contract factory <br>

![d17](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/7fc55722-5fd4-48ef-bc7e-579ed17ae4f5)


if we look inside our ABI piece here <br>

We can see it has ton of information of different functions that we can call <br>

the types that it hs has , return type etc <br>

![d18](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/9376152a-bc1d-4f7d-ae03-0b1da9ebe86b)

We have changed it from .abi to .json <br>


![d19](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/aeb102c8-e641-4bd9-988e-f9f9af5c1f50)

then we will click ```Ctrl + S ``` and the above code will be readable <br>

![d20](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/b104c0cb-95bc-495f-a509-988b6a8f6e60)

Here the above block of code defines what retrieve function can or can't do <br>

![d21](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/e7e642cc-d948-4cbc-8562-3a872ef32360)

Now i changed it back to abi <br>

![d22](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/ca5b08da-71e6-4fba-8cb6-74529a4b3469)

If we give our code just this huge byte code thing it gonna be really hard <br>]
for any processor to decompile this or understand what is going here <br>


![d23](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/10f0c428-da75-436b-9771-5954d5d6b370)

The binary shown left is the abi which is shown right <br>


When we deploy this bytecode on blockchin and when we call functions on it <br>
the code will automatiaclly allow those funtions to get called if they do exists <br>

but in order for our code to know they exist it is much easier just to give it the ABI <br>


![d24](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/67a0745e-295e-4b6d-99ea-954e43d449f2)

Now we gonna conncet tour ganache instance 

![d25](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/3d387b9a-0d74-44b2-8c09-90fd2ad3d8cf)

We gonna collect a wallet with a private key  <br>

![d26](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/010ea6b5-552a-4aa2-baf0-054d78743c5d)

we gonna grab the abi and binary <br>


![d27](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/d499bd2f-1f73-45eb-bc25-58b987eaf709)

And connet abi and  binary to Contractfactory which is also connect to that wallet <br>

that wallet will be the one to actually deploy the contract <br>


![d28](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/0fcb2782-55d2-4095-877e-f4685747d843)

We wil deploy the contract by using the above line of code <br>

![d29](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/9d2ce158-a28d-4d6f-a86f-c72f9092d892)

We will wait one block for that transaction to finish <br>


![d30](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/49220c6b-f105-4730-8c3d-b2d6baf6049d)

Then we will call the above function to return our current favorite number <br>

![d31](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/0edf1276-b865-46ec-a2ff-5b759b1b4be4)

here we can see that retrieve is a view function <br>


If viw and pure function are called outside of the contarct function call <br>

It will not cost any gas <br>


We are just reading of the blockchain but not changing any variable on chain  <br>

So retrieve function will not cot any gas <br>

![d32](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/3483556e-bb3b-4ba3-a1b3-e44f0615914c)
thus our contract  is successfully deployed <br>

and we get this big number response <br>

BigNumber is a library that comes with ethers application that helps us work with numbers <br>

we can find it at this link https://docs.ethers.org/v5/api/utils/bignumber/ <br>


























