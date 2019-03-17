# PGP Backup & Restore w/ GPG
Some helpful commands for future reference.

### Backup
`gpg --armor --export > pgp-public-keys.asc`
`gpg --armor --export-secret-keys > pgp-private-keys.asc`
`gpg --export-ownertrust > pgp-ownertrust.asc`

### Generate Revocation Cert
List keys
`gpg --list-keys`

Generate revo cert
`gpg --armor --gen-revoke [KEY_ID] > pgp-revocation.asc`

### Restore Keys
`gpg --import pgp-public-keys.asc`
`gpg --import pgp-private-keys.asc`
`gpg --import-ownertrust pgp-ownertrust.asc`

### Revoke cert
`gpg --import pgp-revocation.asc`


Commands courtesy of https://msol.io/blog/tech/back-up-your-pgp-keys-with-gpg/