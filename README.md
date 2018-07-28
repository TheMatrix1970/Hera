Hera

Shell script to install a Hera Masternode on a Linux server running Ubuntu 16.04. Use it on your own risk.
Installation

wget -q https://raw.githubusercontent.com/zoldur/Hera/master/hera_install.sh
bash hera_install.sh

Desktop wallet setup

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:

    Open the Hera Desktop Wallet.
    Go to RECEIVE and create a New Address: MN1
    Send 6000 HER to MN1. You need to send all 6000 coins in one single transaction.
    Wait for 15 confirmations.
    Go to Help -> "Debug Window - Console"
    Type the following command: masternode outputs
    Go to Masternodes tab
    Click Create and fill the details:

    Alias: MN1
    Address: VPS_IP:PORT
    Privkey: Masternode Private Key
    TxHash: First value from Step 6
    Output index: Second value from Step 6
    Reward address: leave blank
    Reward %: leave blank

    Click OK to add the masternode
    Close and open the wallet again.
    Go to Masternodes -> My Master Nodes tab
    If you don't see your masternode, click Update
    Unlock your wallet if it is encrypted
    Select your masternode and click on Start
    Login to your VPS and check your masternode status by running the following command. If you get Status 9, it means your masternode is active.

Herad masternode status

Usage:

Herad masternode status  
Herad getinfo

Also, if you want to check/start/stop Hera, run one of the following commands as root:

systemctl status Hera #To check if Hera service is running  
systemctl start Hera #To start Hera service  
systemctl stop Hera #To stop Hera service  
systemctl is-enabled Hera #To check if Hera service is enabled on boot  
