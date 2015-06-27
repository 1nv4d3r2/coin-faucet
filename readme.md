# Coin Faucet

### INSTALL:
Download project & unzip to your web server root directory (ie. www) 

### Edit config.php 
	- $don_faucet: Coind address label used for donations/payouts.
	- $btclogin:   RPC User/Pass settings
	- $sqllogin:   Database user/pass settings

### Add remote IP to access admin/server panel 
 	- Edit header.php to include remote IP for Server/Admin panel access (Line 96)
	- Edit server.php to accept remote IP for Server/Admin panel access (Line 21)

### Database
	- Create SQL user matching config and grant full permissions to faucet database:
	- CREATE USER 'username'@'localhost' IDENTIFIED BY 'mypass';
	- GRANT ALL ON dbname.* TO 'user'@'localhost';

#### Import faucet.sql to your database:
	- Change to "core" directory
	- mysql -u user -p database < faucet.sql
	
Or if you are using a GUI frontend (PHPMyadmin, ADminer, etc) just create the database, then import the .sql file into it.

### Notes:
Whatever account name you set in the config file, must correspond to the actual Wallet name in the daemon. I.E. A wallet labeled 'FaucetWallet' in the config, must have the same name (FaucetWallet) in the wallet's Daemon.

### Donate:
BTC: 1Dh4Ct1xEDi1e4RE8Fqv5YB8EVyQQDuD8V
