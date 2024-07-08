Task 1: we need to downloaded the video by using python code for this we need the following steps.
1. Downloading a File Using requests
Import the requests library: bold text Define a function to download a file:

2. This function takes two arguments:
url: The web address of the file you want to download. output_path: The local path where you want to save the downloaded file.

3. Make an HTTP GET request:
This line sends an HTTP GET request to the specified url. The stream=True parameter tells requests to download the content in chunks instead of loading the entire file into memory at once. This is useful for downloading large files.

4. Opening a File in Write-Binary Mode:
This line opens a file at the specified output_path in write-binary mode ('wb'). The with statement ensures that the file is properly closed after the operation, even if an error occurs.

5. Writing the Content in Chunks:
response.iter_content(chunk_size=1024) returns an iterator that yields chunks of the response content, each chunk being 1024 bytes in size. The for loop iterates over these chunks. if chunk: checks if the chunk is not empty. file.write(chunk) writes the chunk to the file.

6. Printing a Success Message:
This line prints a message indicating that the video has been downloaded successfully and specifies the file path where it was saved.

7. Example Usage:
video_url: The URL of the YouTube video to be downloaded. output_file: The path where the downloaded video will be saved. download_video(video_url, output_file): Calls the download_video function with the specified video_url and output_file.
