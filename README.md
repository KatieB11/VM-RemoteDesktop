
![images](https://github.com/KatieB11/Images/assets/166656124/3869f9fe-b51f-4c04-b8bb-64367b6aaaf7)
</p>



<h1>Azure Virtual Machines Set Up and Remote Desktop</h1>
Want to fire up a virtual machine (VM) on Microsoft Azure and control it remotely? This guide will show you how to create a Resource Group, deploy a VM within it, and access it securely using Remote Desktop.  By following these steps, you'll have a fully functional VM in Azure, ready for remote management through a familiar graphical interface.

<h2>Environments and Technologies Used:</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop

<h2>Operating Systems Used: </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites:</h2>

- Active Azure Tenant and Subscription
- Remote Desktop Connection Software

<h2>Create the Virtual Machine in Azure</h2>

![VM Step](https://github.com/KatieB11/Images/assets/166656124/122a49b5-97ab-42b7-ac58-d172932a28ff)

1 - Navigation: Locate "Virtual machines" in search function and click "Create" and select "Azure virtual machine" to initiate VM creation.

2 - Resource Group: Choose "Create new" for the resource group and assign a name (e.g., VirtualMachine). Resource groups organize Azure resources.

3 - VM Instance Details: Provide a unique VM name (e.g., VM). This identifies your virtual machine within Azure.

4 - Configuration: Proceed with VM configuration options like size, operating system, and network settings.

![Resourse Group Step](https://github.com/KatieB11/Images/assets/166656124/6b14c1d9-f05e-47f1-9e51-2ba7d235282f)


![Size Step](https://github.com/KatieB11/Images/assets/166656124/a8b2226e-6bba-4dac-baf6-f7547198e7e5)

*Remember to click the checkmark at the bottm!

After clicking 'next' for disk and then 'next' for Networking, you'll see that it sets up a virtual network, subnet, and Public IP address automatically. These ensure secure communication for the virtual machine (VM) with other resources or the internet if required. While a public IP isn't mandatory, it's necessary for accessing the VM via Remote Desktop Connection from the internet. You can then adjust settings like the Network Security Group (NSG), which controls traffic to the VM. Remember to allow inbound traffic on TCP port 3389 for remote desktop connection. Finally, click 'review and create'.

![Validation Passed - Keep in mind the price of the VM](https://github.com/KatieB11/Images/assets/166656124/53c18391-a1d2-41d0-8a4f-540eb3abf214)

Once you've confirmed the completion of the Virtual Machine creation process, navigate back to the search tab and enter "Virtual Machines". Select your newly created VM, and you'll find all the essential details, including both public and private IP addresses, which you'll need for Remote Desktop.

![VM IP Addresses](https://github.com/KatieB11/Images/assets/166656124/61b7bb7f-8bad-4776-9854-bf9889fa37d3)

Now that the setup is complete and the Virtual Machine is ready, we'll copy its public IP address and proceed to the Remote Desktop Connection Client. If you're using Windows, you can find the Remote Desktop Connection by searching in the Start menu.

![Remote Desktop](https://github.com/KatieB11/Images/assets/166656124/10e3b559-7034-4de4-823f-e46bbffbe1c6)

![Remote Desktop Connection](https://github.com/KatieB11/Images/assets/166656124/9e508b23-7b75-447c-affe-0c36e8f83b2d)


After launching the Remote Desktop Client, select "add PC" and input the public IP address of your VM. Next, provide the username and password configured during the VM setup. You might receive a warning about an unverified certificate; simply proceed by clicking "connect" as this is normal. Go ahead and click "connect".

![Sucessfully Connected to VM](https://github.com/KatieB11/Images/assets/166656124/ce6f9d53-6a46-47f7-8fe8-d628bbd63f72)

If you've reached this screen, congratulations! You've completed all the essential steps to create and configure a virtual machine in Azure and access it remotely. Now that the VM is up and running, you'll want to configure the operating system. This involves tasks such as setting up additional user accounts for multiple users, installing required software and updates to keep the OS current, and adjusting system settings to meet your specific needs, such as network and firewall configurations.
