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

































