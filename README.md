🌟 Step-by-Step Guide to Building an Eye-Catching Portfolio Website 🌟
If you're ready to showcase your skills and projects with a professional portfolio, here’s your ultimate guide! 🚀

🔖 Step 1: Plan Your Portfolio
1. Plan Your Portfolio Structure
📝 Decide what to include in your portfolio:
🖥️ Header: Include your name, title, and navigation links.
📖 About Me: A brief intro about yourself.
💼 Projects: Add images and descriptions of your work.
💡 Skills: Highlight your technical expertise.
📬 Contact: Provide a way for people to reach you.

2. Create a Virtual Machine (VM) to Host Your Server
Step 2.1: Choose a Cloud Provider
🔧 Popular cloud platforms to create a VM include:
AWS: EC2 (Elastic Compute Cloud).
Azure: Virtual Machines.
Google Cloud: Compute Engine.
Oracle Cloud: Always Free Tier.

Step 2.2: Create a VM Instance
💻 Example with AWS EC2:
Log in to AWS Management Console.
Navigate to EC2 Dashboard: Click "Launch Instance."
Choose an AMI: Select Ubuntu Server (recommended: Ubuntu 22.04).
Select Instance Type: Start with t2.micro (free tier eligible).
Configure Key Pair: Create a key pair or use an existing one.
Network Configuration: Allow HTTP (port 80), HTTPS (port 443), and SSH (port 22) in the security group.
Launch the Instance.

Step 2.3: Connect to Your VM
Use the terminal to SSH into the server:
ssh -i <your-key.pem> ubuntu@<your-instance-public-ip>

3. Install Apache on the VM
Update and Install Apache:

sudo apt update && sudo apt upgrade -y
sudo apt install apache2 -y
Enable and Start Apache:

sudo systemctl enable apache2
sudo systemctl start apache2

Enable apache2 server
Verify Installation:
sudo systemctl start apache2
sudo systemctl enable apache2

Open a browser and enter the public IP of your VM to see the Apache default page.
http://54.151.85.199/

💻 Step 4: Choose Your Tech Stack
Select the tools to build your portfolio:
HTML/CSS: For structure and styling.
JavaScript: Add interactivity.
Bootstrap: Simplify responsive design.
Tip: Experiment with frameworks like React or TailwindCSS for advanced customization. 🎨

🛠️ Step 5: Set Up Your Development Environment
Create a Project Folder:
mkdir website-portfolio
cd website-portfolio

Downloaded the project files from GitHub:
Steps to Handle the main.zip File
Download the Zip File (if not already downloaded): Use wget to download the file:

wget https://github.com/etaoko333/website-portfolio/archive/refs/heads/main.zip
ls -lrt

If unzip is not installed, you can install it:
sudo apt update
sudo apt install unzip -y
unzip main.zip

To edit the code file
cd ~/website-portfolio/
Editor
vim (the file name)

Move out of the website-portfolio-main directory:
cd ..

Move the Extracted Files: After extraction, you’ll find the contents in a directory, likely named website-portfolio-main. Move the files to your desired location, such as /var/www/html:
sudo mv website-portfolio-main/* /var/www/html/

Verify the Files are Moved: Check the target directory to ensure the files are there:
ls -lrt /var/www/html/

🎨 Step 5: Design & Build
Create the Layout: Use HTML to define sections like Header, About Me, Projects, Skills, and Contact.

🔍 Step 6: Test Your Portfolio
📱 Responsive Testing: http://54.151.85.199/

🚀 Step 7: Deploy Your Portfolio
Choose your hosting platform:
Go to aws and buy domain and create record, edit with your ip address.

To install Certbot along with the Apache plugin, run the following command: 
Follow the propmt
sudo apt update
sudo apt install certbot python3-certbot-apache -y

Step 2: Obtain an SSL Certificate
Once the installation is complete, you can obtain an SSL certificate with the following command:
sudo certbot --apache

Step 3: Follow the Prompts
Certbot will prompt you for your email address (for urgent renewal and security notices).
You will also need to agree to the terms of service.
Certbot may ask you if you want to redirect HTTP traffic to HTTPS. This is usually recommended.

Step 4: Set Up Automatic Renewal
Certbot sets up a cron job for automatic renewal, but you can verify it by running:
sudo certbot renew --dry-run

Step 5: Verify SSL Configuration
After successfully obtaining your SSL certificate, you can verify that your site is accessible over HTTPS by visiting:
https://54.176.225.99

✨ Conclusion
By following these steps, you'll have a sleek, professional portfolio to showcase your skills and projects. Customize it with animations, unique color palettes, or even advanced features like dark mode. 🌗

https://eta-oko.com
