# Simplified GPG Command-line Interface

A collection of wrapper scripts to use gpg without its complexities.

## SGPG scripts

Here is how to use these scripts:

```sh
# create <key name>.public.asc and <key name>.private.asc
create-key <key name>
# output a PGP MESSAGE block
cat message | encrypt <public key>
# output the decrypted message
cat encrypted | decrypt <private key>
# create a PGP SIGNATURE block in <message>.asc
sign <private key> <message>
# print "success" if the signature in <message>.asc is a signature of <message> made with the private key
verify <public key> <message> && echo success
```

## Simplified away

- gpg home directory
	- keys are just files
- trust levels
	- you should know whether you trust a key or not
- choice of algorithms
	- the default behaviour (RSA everywhere) is fine for most purposes
- signing options
	- a signature is just a signature in a file, and does not include the signed data

Some other advanced features may be missing.
