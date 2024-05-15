# Exercise 3: Create a Single pane of glass-managed solutions with Azure Arc 
 
## Task 1: Create a Single Pane of Glass Dashboard 
 
1. Navigate back to Azure Portal which you have already opened in the previous exercises. 
 
2. In the Azure portal, Select **Dashboard** on the navigation pane.   

    ![](media/Ex2-Task1-Step2.png)  
 
3. In the Dashboard page, click **+ Create**. 
 
    ![](media/Ex2-Task1-Step3.png) 
     
4. In the Create a dashboard page, select **Create a custom dashboard**. 
 
    ![](media/Ex2-Task1-Step4.png) 
 
## Task 2: Adding Resource Graph Grid Tiles 
 
1. On the Right side of the custom dashboard page, under **Tile Gallery** search for **Resource graph grid tile (1)**, select **Resource graph grid tile (2)**, click on the **Add (3)** button, and click on **Save (4)**. 
 
    ![](media/Ex2-Task1-Step5.png) 
     
2. In Dashboard page, under **Resource graph grid tile** click on **Configure tile**.
 
    ![](media/Ex2-Task1-Step6.png)  
     
3. Minimize the Azure Portal Browser window. 
  
4. From LAB VM, open **File Manager**, navigate to `C:\LabFiles\Azure-Arc-enabled-SQL-Server-main\lab-files`. 
  
    ![](media/Ex2-Task1-Step8.png)  
  
5. Open the **Servers** script file by right-clicking on the file, select **Open With**, and then select **Notepad**. 
 
    ![](media/Ex2-Task1-Step9a.png)  
     
    ![](media/Ex2-Task1-Step9b.png)  
     
6. Copy the SQL query from the **Servers** file, and overwrite the sample query with the Servers query in the Dashboard query section. 
 
    ![](media/Ex2-Task1-Step10.png)  
     
7. Click on **Run Query**, You should see something like the below with the SQL Servers you installed the **Azure Arc SQL Agent** as well as **Azure SQL Servers** running in Azure and update the tile in the dashboard by selecting **Update pinned part on dashboard**. 
     
    ![](media/Ex2-Task1-Step11.png)  
     
8. In Dashboard page, click on **Edit**, go back and follow **Step 1** to **step 4**, and continue from **step 9**.
 
     ![](media/Ex2-Task1-Step12.png)  
     
9. Open the **Databases** script file by right-clicking on the file, select **Open With**, and then select **Notepad**. 
 
10. Copy the SQL query from the **Databases** file and overwrite the sample query with the Servers query in the Dashboard query section. 
 
11. Click on **Run Query**, You should see something like the below with the SQL Servers you installed the **Azure Arc SQL Agent database** as well as **Azure SQL Servers base** running in Azure and update the tile in the dashboard by selecting **Update pinned part on dashboard**. 
     
    ![](media/Ex2-Task1-Step15.png)   
          
## Task 3: Adding Resource Graph Grid Tiles      
     
1. In Dashboard page, click on **Edit**, under **Tile Gallery** search for **Resource graph chart tile (1)**, select **Resource graph grid tile (2)**, click on **Add (3)** button, and click on **Save (4)**. 
 
    ![](media/Ex2-Task3-Step1.png) 
     
2. In Dashboard page, under **Resource graph chart tile** click on **Configure tile**. 
 
    ![](media/Ex2-Task3-Step2.png)  
     
3. Minimize the Azure Portal Browser window. 
  
4. From LAB VM, open **File Manager**, navigate to `C:\LabFiles\Azure-Arc-enabled-SQL-Server-main\lab-files`. 
   
5. Open the **Server by location Chart** script file by right-clicking on the file, select **Open With**, and then select **Notepad**. 
      
6. Copy the SQL query from the **Server by location Chart** file, and overwrite the sample query with the Servers query in the Dashboard query section.  
 
7. Click on **Run Query** and update the tile to **Charts (1)** and select **Bar chart (2)** in the dashboard by selecting **Update pinned part on dashboard (3)**. 
     
    ![](media/Ex2-Task3-Step7.png) 
 
8.  Your dashboard should look like the one below. You can resize each individual tile and arrange them however you like on your new dashboard by clicking edit at the top of the dashboard. 
     
    ![](media/Ex2-Task3-Step8a.png) 
     
    ![](media/Ex2-Task3-Step8b.png) 
     
    ![](media/Ex2-Task3-Step8c.png)   

9. This repo [https://azure.github.io/az-hop/user_guide/files.html](https://github.com/markm555/SQLSPOG) contains all the scripts. The scripts are regularly updated.
