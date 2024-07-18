# Twitter Video Downloader

This project provides a script to download videos from Twitter using the tweet URL. The script uses the Twitter API to retrieve the video URL and `ffmpeg` to download and save the video locally.

## Features

- Extracts video URLs from Twitter tweets.
- Downloads videos using `ffmpeg`.
- Provides detailed debug logging for troubleshooting.
- Handles various edge cases and errors gracefully.

## Prerequisites

- Python 3.6+
- `ffmpeg` installed and available in the system's PATH.
- Required Python packages listed in `requirements.txt`.

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/mostafabadrshaalan/twitter-video-downloader.git
    cd twitter-video-downloader
    ```

2. Install the required Python packages:
    ```sh
    pip install -r requirements.txt
    ```

3. Ensure `ffmpeg` is installed and accessible from the command line:
    ```sh
    ffmpeg -version
    ```

4. Create and update the `settings.json` file in the `src` directory with your desired configuration:
    ```json
    {
        "gif": {
            "convert_gif_flag": true
        },
        "ffmpeg": {
            "loglevel": "info"
        },
        "image": {
            "save_option": "all"
        },
        "debug_option": true
    }
    ```

## Usage

To download a video from Twitter, use the script as follows:

1. Set the `tweet_url` and `output_filename` in the script:
    ```python
    if __name__ == "__main__":
        tweet_url = "YOUR_TWEET_URL_HERE"
        output_filename = "output_video"
        get_video(tweet_url, output_filename)
    ```

2. Run the script:
    ```sh
    python download_video.py
    ```

3. The video will be saved to the specified output file.

## Debugging

If `debug_option` is set to `true` in `settings.json`, a debug log will be generated and saved to `debug.log` in the project directory. This log contains detailed information about the script's execution and can help troubleshoot any issues.

## Contributing

Contributions are welcome! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a new Pull Request.


## Acknowledgments

- [ffmpeg](https://ffmpeg.org/) for video processing.
- [requests](https://pypi.org/project/requests/) for HTTP requests.

