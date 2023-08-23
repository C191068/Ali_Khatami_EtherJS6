![image](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/30951282-19a0-4df5-b46b-984e1f580d8c)# Ali_Khatami_EtherJs6(Learning from the video of Patrick Collins)

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

![d33](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/0551764c-d8e7-490d-8885-214ff269c563)

they also ahve a section called ```Why can't I just use numbers?``` <br>

![d34](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/d558fe01-8cae-4f4c-8c03-e78fda0bf66f)

We expect the currentfavorite number to return zero but return this weired hex thing <br>

So solidity can't use decimel places and javascript has a hard time with decimel places  <br>

and this can be more rational for why not to use numbers <br>

Most of the time we will see instaed of numbers we will see strings <br>


we will see javascript use strings like this  ``` "100000000000" ```  <br>

![d35](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/72b26c94-1464-4997-93f5-89a80a2e5ea1)

We have made it more readable by adding toString() at the end <br>

to print out the string version of the favorite number <br>

![d36](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/acf526a2-6e73-46e9-9067-f8ef9208b464)

Now if we re run this code we get zero which make sense because our favorite number get initialized to zero <br>


Now just amke our console.log a little bit more syntactical <br>

We can use something called string interpolation <br>

So we can interpolate our string with variable and use the backtick symbol  <br>

![d37](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/2c2a7735-7a94-4df4-bff8-82a9629c4895)

So we use the above code and tell javascript that it is a variable that we want to read <br>


![d38](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/c25ba7a4-69b7-45f9-b922-bbb87f7dcb0c)

We put some dollar sign and bracket here <br>


![d39](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/86dbbfc6-d1a4-47c0-a573-972206b06e51)

we can get current favorite number equal to zero <br>


Now we wil update the contract by calling the store function <br>


![d40](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/f5caa9aa-a36c-4144-970d-037c3b459a85)

It is better to pass number as strings to contract functions  <br>
Those will be little bit confusing than if we use numbers <br>

Ethers is smart enough to know that that the aboe 7 string is actually <br>
7 the number <br>

![d41](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/8ccb5776-19a1-41e7-811d-b9d43e0d6e3d)

here we have to wait for one block confirmation <br>


![d42](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/e74e56f8-3dfa-4359-9b10-c7c84a58a674)

It is similiar to the above <br>

But little bit different because first one is using contract.factory and another is using <br>
function of the contract <br>

When we call the function on the contract we get transaction response <br>

When we wait for the transaction to finish we get transaction receipt <br>

![d43](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/13cbb023-b13c-47cf-ac31-37f57ffa2ced)

Then we use the above line of code to update favorite number <br>

![d44](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/7a9b21ce-3acc-4d4f-96e8-55874b6a8244)

then we use the above line of code for output at console <br>

In this process we are doing the following <br>


![d45](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/0ffa040e-57d0-4e49-ae7c-c4318162cba0)

we are deploying the contarct <br>


![d46](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/33504a4f-199f-41b1-9db4-e7e822418692)

we are gettuing the initial value <br>

![d47](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/09815462-e2f1-4cd7-ab66-e49d6be133cb)

We gonna update our contarct by calling store which is gona cost gas  <br>

So this is a transaction <br>


![d48](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/353d821a-a3f1-4758-b3d0-29b403254ade)

Then we gonn aget the transaction receipt and we are not gonna do  <br>
anything with the transaction receipt <br>

![d49](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/44cb2515-1684-48a4-a3f0-73f748184f6f)

Then we get the updated favorite number and we will just print it out <br>

![d50](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/9f78a5d6-c94b-4a16-bca7-3abb074751a2)

At last successfully we get the updated favorite number <br>


![d51](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/07403e33-b7c9-49ba-b7d7-76b5326b23b8)

We can see at our ganache transaction we now have a contract call at the top <br>

![d52](https://github.com/C191068/Ali_Khatami_EtherJS6/assets/89090776/4b874666-d833-4628-86b2-840514ef9215)

here we can see the transaction data <br>

This transaction data is what get sent at data slot of our transaction object <br>





























