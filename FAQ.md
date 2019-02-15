# FAQ

## Q1: What's the routable network?
**A1:** Every project has its own routable network. There is already one device up and running, which lives outside of your
VMware project. That device is the gateway, it will route traffic. You received the IP of the gateway via mail together with the login.

## Q2: We don't get an IP on our routable network via DHCP.
**A2:** Correct, there is no DHCP server on the routable network. The gateway, which is already there, only provides routing. Therefore, all servers should have a static IP address.
You received the project range via mail together with the login.

## Q3: The other networks don't have internet access.
**A3:** Correct, you have to setup your own routing towards the routable network. **Pro-tip: Use Network Address Translation (NAT)**

## Q4: How can I create a new VM?
**A4:** **First of all use the HTML web interface or the API.** There are two ways to create a new VM. The preferred manner is to create a VM from an existing template. There are a few templates available. You can view them in the second tab (VMs and Templates). There should be a folder called `Templates`. Just right click on the preferred template and `New VM from this Template...`.

The second way to create a VM is from scratch with an ISO. The ISO files can be found on each of the three `Local  compute datastores` under the directory `isos`. When you create a new VM, select at step `7 Customize hardware` under `New CD/DVD Drive *` the option `datastore ISO file`. Note: only the datastore where the VM will be made is accessable in this window. (We don't want to install a VM using an ISO file located on another Compute node now, do we?). Select the ISO file of your choosing. **Do not forget to check `☑ Connect At Power On` before continuing to step 8!!!**

## Q5: Where can I find the ISO files to install a new Virtual Machine?
**A5:** The ISO files can be found on each of the three `Local  compute datastores` under the directory `isos`.

## Q6: I want the ISO for an other distribution...
**A6:** Upload it yourself to your own storage or contact Tim and maybe he will upload the iso to the shared datastores.

## Q7: Can we have a real public IP address?
**A7:** No.

## Q8: How can we communicate with Tim?
**A8:** He'll be as much as possible available during the Research Project hours.

## Q9: What are the credentials of the templates?
**A9:** For the `-base-` templates it's: Login: `user`, password: `user`. For the  template `CnA-Jumpbox`, it's: Login `ansible` password: `test`. Why so unsecure? To trigger you to change it **immediately**!