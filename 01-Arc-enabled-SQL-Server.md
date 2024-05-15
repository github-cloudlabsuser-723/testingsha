# Exercise 1: Onboard the On-prem SQLServer to Azure Arc enabled SQL Server 
 
In this exercise, you will onboard SQL Server to Azure Arc using PowerShell commands to Azure Portal. 
 
## Task 1: Login to Azure Portal in SQL Server via Hyper-V Manager 

1. In the Azure portal, click on the search blade at the top and search for ```SQL Server```. Then select **SQL Server - Azure Arc**. 
  
   ![](media/EX1-Task1-Step2.png) 
    
1. Click on the **Add** button to create the **SQL Server- Azure Arc**.  
  
   ![](media/az-arcv-m.png) 
    
1. In the Adding existing SQL Servers instances page, click on **Connect Servers**. 
 
   ![](media/EX1-Task1-Step4.png) 
    
1. You will now see the prerequisite page. You can explore the page and then click on the **Next: Server details** option. 
     
   > **Note**: We have already completed the prerequisite part for you.  
     
   ![](media/EX1-Task1-Step5.png) 
    
1. On the **Server Details** blade, enter the details below. 
  
   - Subscription: Select the default subscription.
   - Resource group: Select **sql-arc** from dropdown list. 
   - Region: **<inject key="Region" enableCopy="false"/>**. 
   - Operating Systems: Select **Windows**. 
   - Server Name: Enter **SQLVM**.
   - License Type: Select **I want to license my production environment on this server with Enterprise or Standard edition using pay-as-you-go ("PAYG")**. 
 
     Now, click on the **Next: Tags** button. 
    
   ![](media/sqlarcdetails.png) 
    
1. Leave the default for tags blade and click on **Next: Run Script** button. 
  
1. On the **Script** blade, explore the given script, copy the script by clicking **Copy to Clipboard** paste the code into the notepad. We will be using this PowerShell script to **Register Azure Arc enabled SQL Server** later.  
       
      ![](media/EX1-Task1-Step8n.png) 

1. Minimize the Browser window.  

1. In the **LABVM**, open the **Start menu** and search for **Hyper-V**. Select **Hyper-V Manager**. 
 
      ![](media/EX1-T1-S1.png "search hyperv") 
 
1. Then, you need to Select LABVM-<inject key="Deployment ID" enableCopy="false"/> to connect with the Local Hyper-V server. 
 
      ![](media/EX1-T1-S2.png "select server") 
 
1. On the Hyper-V manager, you will find multiple guest virtual machines available. 
 
      ![](media/number-of-hyper-v.png "select VM") 
       
1. Open **sqlvm** from the Hyper-V Manager by double clicking on **sqlvm**. 
 
      ![](media/sql-vm.png "open VM")  

   >**Note**: Please start the **sqlvm** if it is stopped state.
 
1. Connect to sqlvm box, and then click on the **Connect** button. 
 
      ![](media/EX1-T1-S5.png "open VM") 
 
1. Type password **demo@pass123** and press **Enter** button to login. Then, you can resize the sqlvm window size at your convenience. 
 
      ![](media/EX1-T1-S6.png "open VM") 
             
## Task 2: Register Azure Arc-enabled SQL Server. 
  
1. From the start menu of the SQL VM, search for **PowerShell**, and right click on **Windows PowerShell ISE** and select **Run as Administrator**. 
  
   ![](media/Ex1-Task2-Step2.png) 
   
1. In Windows PowerShell ISE, click on **Show Script Pane**. 
  
    ![](media/Ex1-Task2-Step3.png)        
 
1. The script you copied on **step 8 of task 1** must be pasted in **Script Pane** and clicked on **Run Script**. 
 
    ![](media/Ex1-Task2-Step4.png)  
      
1. After running the command, you will see some outputs which show that the script started running. 
   
    ![](media/Ex1-Task2-Step5.png) 
 
1. Copy the **authenticate code**. 
 
    ![](media/Ex1-Task2-Step6.png) 
 
1. In Hyper-v VM, use a web browser to open the page **https://microsoft.com/devicelogin**, enter the **authenticate code** and click on **Next**.  
 
    ![](media/Ex1-Task2-Step7.png) 
  
1. On the **Sign in** tab, You're signing in to **Microsoft Azure Cross-platform Command Line Interface**‭. Enter the following **Email/Username** and then click on **Next**.  
   * Email/Username: <inject key="AzureAdUserEmail"></inject>
   
       ![](media/sqlarclogin.png "Enter Email")
    
1. Now, enter the **Password** that you have already received for the above account. 
      
   * Password: <inject key="AzureAdUserPassword"></inject> 

      ![](media/sqlarcpassword.png "Enter Password")
      
1. In Are you trying to sign into Microsoft Azure CLI? Click on **Continue** and minimize the Browser window. 
 
    ![](media/Ex1-Task2-Step9.png) 
 
1. In 5-10 minutes, you will see that the script execution is completed. Make sure that you see the following output: ```SQL Server is successfully installed``` 
 
    ![](media/Ex1-Task2-Step10.png) 

1. Minimize the sqlvm on LABVM-<inject key="Deployment ID" enableCopy="false"/>    

    ![](media/sqlvm-min.png) 

1. Bring back the browser window where you had opened Azure Portal and search for **SQL Server -Azure Arc**. If you are already on that page, you will need to click on the Refresh button. On that page, you will see one resource **SQLVM** that we just created using the PowerShell script in the previous step. 
 
    ![](media/Ex1-Task2-Step11.png) 
   
1. Here you can explore the Azure Arc | SQL Servers blade, click on **SQL Servres instances** **(1)** under Infrastructure from left-menu. By selecting the **+ Add** **(2)** option from the top menu you can onboard SQL Servers to Azure. You can run SQL queries by clicking on **Open query** **(3)** with ad-hoc method to access the data of a remote server. At last, you can see the SQL Servers that are onboarded to Azure Arc **(4)** as shown in the below screenshot.

    ![](media/sql-arc-overview.png)

1. Select the **SQLVM** resource and now you can see the dashboard of **SQLVM** SQL Server -Azure Arc from Azure Portal. 
 
    ![](media/Ex1-Task2-Step12.png)    
    
1. Now, click on Next from the lower right corner to move on to the next page.

<validation step="f00aaa9f-7a98-4314-9310-a1fcd61130aa" />
