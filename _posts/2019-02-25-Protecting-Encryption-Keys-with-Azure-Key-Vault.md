# [Protecting Encryption Keys with Azure Key Vault - Stephen Haunts](https://www.meetup.com/dotnetnotts/events/258787042/)

> In a world where we are putting our companies data in the cloud, the protection of that data against a data breach has never been more important. In this talk Stephen will show you how to setup and use the Microsoft Azure Key vault to protect your encryption keys and secrets like passwords and connection strings. Azure Key Vault uses the power of Hardware Security Modules (HSM's) to protect your secrets and make sure your solutions are as secure as they can be when working in regulated industries like healthcare, financial and insurance.

> As well as showing you how to setup and configure the vault, Stephen will show you how to code against it and various different patterns for security in a cloud base multi tenant environment. Stephen will cover topics like:
> * Setup Azure key Vault
> * Authorize your application to access the vault with AzureAD
> * Accessing the vault from your applications
> * Using the Vault to wrap local encryption keys for performance
> * Encrypting connection strings as Key Vault secrets to get flexible database routing in the cloud
> * Audit logging for compliance

Stephen introduced his talk with a description of data breach 'costs' and emphasised it's not a case of _if_ a data breach is going to happen but _when_.

An overview was given of symmetric and asymmetric keys where either the whole key was used or a combination of public and private keys. Also of key management and the storing of security certificates.

He talked about the concept of _hybrid encryption_ where various methods were combined to achieve a better result.

We were introduced to **Hardware Security Modules**, physical devices for storing security information which are hack proof, tamper proof and also expensive.

[Azure Key Vault](https://azure.microsoft.com/en-us/services/key-vault/) is a cheaper alternative (with similar offerings from AWS and Google) which provides an abstraction for the physical devices sitting in Microsoft data centres.

Two options are available when using Key Vault: Software (presumably emulation of the physical device?) or Hardware with the latter being the more expensive option so this is probably only justified for production systems.

Once security information is put into the Key Vault then it never comes out again, it's stored encrypted and isn't possible to retrieve. It's also possible to security "secrets" or blobs of text like connection strings or APIs that you don't want to have in source control, particularly if the source code is public.

One of the drawbacks of using Key Vaults is when you have multiple environments, you can't just copy the production database into the dev or test environment to debug something because the security keys should be different for each environment (but you probably shouldn't be copying from production anyway!).

**Local Key Wrapping** is a method of storing an AES key inside the key vault and then decrypting that key to do some work, caching it locally for a period of time, this saves the expense of having to hit the cloud based Key Vault for _every_ encryption operation.

Key Vaults can also be set up to be more granular in the production environment, each customer using a SaaS environment can have their own master keys to make it less likely they are able to see another customers data, effectively partitioning by encryption key.

**Incremental keys** are a method of reducing audit effort for things like PCI compliance, if storing credit card information then Key V1.0 is used for the first 1000 cards, V1.1 for the next 1000 and so forth. If the system is breached then a security key can only access a smaller sub-set of the entire database.

Lastly **Password protection** was discussed with the current "gold standard" being [PBKDF2](https://en.wikipedia.org/wiki/PBKDF2) for storing hashed and salted passwords which are more difficult to crack. The option of storing the salt value inside the Key Vault also makes it harder to decrypt passwords in the event of a breach.

## Links

<https://stephenhaunts.com/>

<https://twitter.com/stephenhaunts>

<https://github.com/stephenhaunts/>

[Azure Key Vault Sample Code](https://github.com/stephenhaunts/AzureKeyVault)

<https://azure.microsoft.com/en-us/services/key-vault/>

[PBKDF2](https://en.wikipedia.org/wiki/PBKDF2)