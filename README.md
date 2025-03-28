# File_Recovery-using-Autopsy

## Aim
The objective of this guide is to demonstrate how to:  
 - Create a **Virtual Hard Disk (VHD)**.  
 - Add images to the disk, delete them, and recover them using **Autopsy**.  
 - Understand the forensic recovery process for deleted files.  
 - Learn how to remove the virtual disk after completing the experiment.

## Virtual Disk Creation & File Recovery using Autopsy 


## Step 1: 
   Create a Virtual Hard Disk (VHD) 

### **1. Open Disk Management**  
- Press **Windows + X** → Click **Disk Management** 

 ![image](https://github.com/user-attachments/assets/dedfe3e3-124b-47a6-8a77-6f5e14ae9de3)

### **2. Create a New VHD**  
- Click **Action** (top menu) → **Create VHD**.  

![image](https://github.com/user-attachments/assets/eb2a9cf6-71e6-462e-96bb-ffd2c449838b)

### **3. Choose File Location & Size**  
- Click **Browse** and select where to save the VHD file (e.g, `C:\new VHD.vhd`)
- Set the **size** (e.g: `1GB`) 
- Choose **VHD (Fixed Size)** and Click **OK**

![image](https://github.com/user-attachments/assets/0edd103e-75c0-47c1-8b6f-9bbcd8330565)

### **4. Initialize the Disk**  
- In **Disk Management**, find your new disk (marked as "Not Initialized").  

![image](https://github.com/user-attachments/assets/6cd94311-2021-4893-b8d2-004b8f3ccedf)

- Right-click the disk → Click **Initialize Disk**.

![image](https://github.com/user-attachments/assets/94808ed3-3c78-4da7-96b7-9b5de195aa04)

- Select **MBR (Master Boot Record)**. 

![image](https://github.com/user-attachments/assets/c9fe320b-c43a-4976-a9fa-6a55db92f1ec)

### **6. Create & Format the Partition**  
- Right-click the **Unallocated Space** → Click **New Simple Volume**.  

![image](https://github.com/user-attachments/assets/4aab04ad-342d-40e9-87f1-88520240e2f2)

![image](https://github.com/user-attachments/assets/fba807a9-8e1f-46c6-8c73-cce754ff963f)

![image](https://github.com/user-attachments/assets/2d0e2562-2a21-4939-b6ea-3ae1230028be)

- Click **Next** → **Click on Mount in the following empty NTFS folder** → **Browse** → **Assign a drive letter (e.g., `C: or D:`)** → **New folder** → **OK**

![image](https://github.com/user-attachments/assets/231dcc71-2b09-427a-97e7-691568f53633)

![image](https://github.com/user-attachments/assets/eab7f3ab-7bf5-4e49-a96d-3eeb3f2242d0)

![image](https://github.com/user-attachments/assets/46ba630a-fe6f-4629-b024-0f8535823d13)

- Click **next** → **Finish**. 

---

## **Step 2: Add & Delete Files for Recovery** 

### **1. Copy Files to the Virtual Disk**  
- Open **File Explorer** → Go to the new drive (`C: or D:`), where the folder created in the previous step
- Create a new folder (`TestFolder`) and copy **images or files** into it.  

### **2. Delete the Files**  
- Select any one or two images → Press **Delete**.  
- Empty the **Recycle Bin** to permanently delete them.  

---

## **Step 3: Recover Deleted Files Using Autopsy**  
### **1. Open Autopsy & Create a New Case** 

- Launch **Autopsy** and **Run as a administrator**  
- Click **Create New Case**.  

![image](https://github.com/user-attachments/assets/98f8abac-039b-4937-9a45-3afdc75d649d)

- Enter a **Case Name** (e.g., `Autopsy1`).  
- Choose a **Case Folder** location.  
- Click **Next** → Click **Finish**.  

![image](https://github.com/user-attachments/assets/4ccd6da5-5056-4fbd-87cc-b53cbabfb365)

### **2. Add the Virtual Disk as an Evidence Source**  
- Click **Add Data Source**  → **Select Host**

![image](https://github.com/user-attachments/assets/8422c766-cf33-461d-96b9-b440ca7fb21b)

- Select **Local Disk** → **next** 

![image](https://github.com/user-attachments/assets/1c4d6ef6-1ea5-44be-8b9b-cd7e6d6319c2)

- Select Disk → **Choose the VHD drive (`Drive1`)**

![image](https://github.com/user-attachments/assets/e3a986a0-6f99-4403-8856-6498c442e19a)

- Click **Next** → Keep default settings → Click **Finish**.  
- Wait for Autopsy to process the disk.  

### **3. Recover Deleted Files**  
- Go to **File Views** (left panel).  

![image](https://github.com/user-attachments/assets/d679b0c4-86a5-41b8-a53a-58038cf0fb8c)

- Click **Deleted Files** → Find your deleted images.  
- Right-click an image → Click **Extract File**.  

![image](https://github.com/user-attachments/assets/cba0d44c-5aed-4eab-af01-145f99bf83b6)

- Select a folder to see the recovered files (e.g., `C:\image_recovery`).  

**Your deleted images are now recovered!**  

---

## **Step 4: Delete the Virtual Disk (Optional Cleanup)** 

### **1. Detach the VHD**  
- Open **Disk Management** (`Win + X` → Disk Management).  
- Find the **virtual disk** (`C: or D:`).  
- Right-click the disk (not the partition) → Click **Detach VHD**.  

### **2. Delete the VHD File**  
- Open **File Explorer**.  
- Go to the location where you saved the `.vhd` file (e.g., `C:\new VHD.vhd`).  
- **Delete** the `.vhd` file.  
- Empty the **Recycle Bin**.  

**Your virtual disk is completely removed!**  
 
---
 ## Output:
 ## FOLDER BEFORE DELETING THE IMAGES:

 ![Screenshot 2025-03-20 141943](https://github.com/user-attachments/assets/5c94732f-c0ca-4783-94fa-e20e89c1e634)
 
## RECOVERY OF THE IMAGES USING AUTOPSY TOOL:
![Screenshot (354)](https://github.com/user-attachments/assets/dbf2b980-6fd5-4f66-ab43-997a7597016b)

## FOLDER AFTER RECOVERY:
![Screenshot 2025-03-20 141943](https://github.com/user-attachments/assets/1e7d7e83-c385-4271-82f1-2b1161c4f846)

## Result :
 This guide covers creating a Virtual Hard Disk (VHD), adding, deleting, and recovering images using Autopsy, and safely deleting the virtual disk after the experiment.
