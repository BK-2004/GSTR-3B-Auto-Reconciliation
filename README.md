📖 The Story Behind the Code
This tool was born out of sheer necessity during my CA articleship at a mid-sized firm. Like many firms, our GSTR-3B reconciliation process was highly manual—downloading returns from the GST portal and copy-pasting every single data point into Excel. During tax audit season, this repetitive task took 20–25 minutes per client, acting as a massive bottleneck and creating room for manual entry errors. Due to strict data privacy policies, the firm couldn't rely on third-party commercial software.

I decided to build a secure, offline solution from first principles.

The Evolution of the Tool:

Data Extraction (Power Query): I started by learning Power Query to automate PDF data extraction. It took months of trial, error, and overcoming data-cleaning hurdles to teach the machine to extract GSTR-3B data flawlessly.

Automating Downloads (RPA & Python): After my articleship, I attended the ICAI Ernakulam Advanced ITT batch, where faculty Vivek Chandran introduced me to RPA. This inspired me to write a Python script to automate the portal downloads, which I further optimized with logical loading buffers.

The Final Integration (VBA + Python): To make the tool completely seamless for end-users, I embedded the Python automation directly inside Excel VBA. The VBA macro dynamically generates a .py file, executes the portal download, and feeds the data into the Power Query engine—all without leaving the GST Reco 3.0 Fy 25-26.xlsm interface.

What started as a way to save 25 minutes of manual copy-pasting has evolved into a robust, automated reconciliation engine. I am open-sourcing it to help other professionals streamline their statutory tax processing securely.

⚙️ Prerequisites
Before using the tool, ensure your environment is set up:

Excel Version: You must use Microsoft Excel 365 or Excel 2016 and later, as the tool relies on Power Query and advanced dynamic array formulas.

Python: Download Python from the official website.

Crucial Step: During the Python installation, you must check the box that says "Add Python to PATH" so Excel VBA can communicate with it.

🚀 How to Use It
Check Compatibility: Open GST Reco 3.0 Fy 25-26.xlsm, enable macros, and run the built-in compatibility check directly within the Excel sheet to verify your environment is configured correctly.

Enter Credentials: Input your GST portal User ID into cell C15 and your Password into cell C17.   

Select Financial Year: Choose your target Financial Year from the dropdown in cell D19.   

Run the Automation: Press the Download 3B button.

Select Save Location: A dialog box will pop up asking you to select the target folder. Once selected, the embedded script will execute, automatically downloading the returns and reconciling your data.
