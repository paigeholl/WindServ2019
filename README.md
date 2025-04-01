# Setting Up a Windows Server 2019 Virtual Environment with VirtualBox

As part of my ongoing exploration of enterprise network environments, I recently built a Windows Server 2019 virtual machine using Oracle VirtualBox. This setup provides an excellent foundation for testing domain configurations, Active Directory implementations, and various Windows Server features without the need for dedicated hardware.

## Initial VM Configuration

The process begins with creating a properly configured virtual machine. From VirtualBox's main interface, I selected "New" from the Details menu to initialize the VM creation wizard.

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_WAxvyzOwUfpHyu6vGz.png)

When naming the virtual machine, I chose a descriptive identifier that reflects its purpose. Since Windows Server 2019 isn't explicitly listed in VirtualBox's OS options, selecting "Other Windows (64-bit)" from the dropdown menu ensures compatibility.

### Hardware Allocation

Resource allocation requires balancing the VM's needs with your host system's capabilities. For a functional Windows Server environment, I allocated 2048MB of RAM and 3 processor cores. This configuration provides sufficient resources for basic server operations while leaving adequate headroom for the host system.

The defaults in the 'Virtual Hard Disk' menu are fine. Select Next

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_NXyaqOP6P2TeFg6P1o.png)

Select Finish

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_7KTFrUycdQHyOuVKF7.png)

Time to Adjust the settings for this VM

Open Settings

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_1VgNdkuJYE2U0T7YgE.png)

Select 'Advanced' and adjust Shared Clipboard and Drag'n'Drop to 'Bidirectional'

- This makes you able to copy and paste in to the VM and drag and drop files, etc. between you VM and home computer

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_vbjO6J4SDDk8SzwkPc.png)

Select 'Network' and adjust Adapter 1 to be 'NAT' and Adapter 2 to be 'Internal Network'

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_VxccyRT5QbKLACd7Na.png)

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_3qczm0hQyAUJ8K00Td.png)

One Adapter is meant for connecting to the internet and one is meant for connecting the internal corporate environment we are creating.

Click OK

Double click the DC to start

Select the downloaded Server 2019 iso from the location you saved it

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_UcG5lDWrUgw0ojkblE.png)

Select Start

Once it starts up select Next

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_sTOUNu5HILIMjXIlKX.png)

Click Install now

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_Lim0zFb1aVF7YURsr5.png)

You select either Desktop experience but I chose the Standard one.

Select Next

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_tUILU97SsWCVzBR3RO.png)

Accept the terms and conditions

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_D9vMh1oAe16aJ89o7d.png)

Choose Custom: Install Windows only

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_f9fn3Xu6wsjIuSdZ32.png)

Select Next

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_GwErftDOH7qBcBcL0b.png)

Let the computer install Windows, it'll restart a few times

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_U9v0oQqelfNnGK36gT.png)

Give this a simple password that you can remember

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_gAlrtz4dTEd4wJi86I.png)

Great now server 2019 is installed!

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_evEeVd2ACp68efD5kX.png)

To press Ctrl+Alt+Del, you have to select Input > Keyboard > Insert Ctrl+Alt+Del

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_JYB4ScqxYb4RFamPJt.png)

Select Yes in Networks pop up

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_2YFkIVjPpR30cOjyBA.png)

Now we will install VM Guest Additions to make the experience more smooth

Select Devices > Insert Guest Additions CD image..

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_9nrIl9pC2wvc9xtFoT.png)

Open File Explorer and under 'This PC' double click 'CD Drive (D:) VirtualBox Guest Addition'

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_nDOCHro8HQSXkhfMAF.png)

Run VBoxWindowsAdditions-amd64 (or the 64bit one)

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_6DnHakmEAT4yHi6B2P.png)

Click Next through all the prompts and Click Install

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_RUFaFUmHD19wVJxSWk.png)

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_DcCBqBdTGkgkAw3aq3.png)

Select you want to Reboot later

Shut down the VM completely and start back up

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_Q3eBvoFxKm7YIqCaik.png)

