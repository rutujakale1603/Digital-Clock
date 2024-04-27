# Digital-Clock
# Internpe project
This Python script creates a simple digital clock that displays the current time in Indian Standard Time (IST) in the format HH:MM:SS AM/PM. Let's break down the code:

1. `import time`: This imports the `time` module, which provides various time-related functions.

2. `digital_clock()`: This is the main function that continuously updates and prints the current time. It works as follows:

   - It initializes the initial time to 10:46 AM in Indian Standard Time (IST). The `time.strptime()` function parses the string representation of time into a `struct_time` object, and `time.mktime()` converts it into epoch time (seconds since the epoch).
   
   - Inside a `while True` loop, it continuously updates and displays the current time.
   
   - It calculates the current time in UTC by using `time.time()` to get the current epoch time. Then, it adds 5 hours and 30 minutes (5.5 * 3600 seconds) to convert it to IST.
   
   - It formats the current time into hours, minutes, seconds, and AM/PM format using `time.localtime()` to get a `struct_time` object and extracting the necessary components.
   
   - The `str.zfill(2)` method is used to zero-pad single-digit hours, minutes, and seconds to maintain a consistent format (e.g., "01" instead of "1").
   
   - It determines whether it's morning (AM) or afternoon/evening (PM) based on the hour value.
   
   - It prints the formatted time using `print()` with `\r` (carriage return) to overwrite the previous output on the same line. `flush=True` ensures that the output is immediately printed without buffering.
   
   - Finally, it waits for one second using `time.sleep(1)` before updating the time again.

3. `if __name__ == "__main__":`: This block ensures that the `digital_clock()` function is executed only when the script is run as the main program, allowing the clock to start when the script is executed directly.

Overall, this script creates a simple digital clock that continuously updates and displays the current time in Indian Standard Time (IST) in the console.
