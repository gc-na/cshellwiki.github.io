# [Linux] Bash at: Schedule commands for later execution

## Overview
The `at` command in Bash is used to schedule commands to be executed at a specified time in the future. This is particularly useful for automating tasks that need to run once at a particular time without requiring user intervention.

## Usage
The basic syntax of the `at` command is as follows:

```bash
at [options] [time]
```

## Common Options
- `-f FILE`: Read commands from the specified FILE instead of standard input.
- `-m`: Send mail to the user when the job has completed, even if there was no output.
- `-q QUEUE`: Specify the queue to use for the job. Different queues can have different priorities.
- `-l`: List the jobs scheduled for the user.
- `-d JOB_ID`: Remove the job with the specified ID from the schedule.

## Common Examples

1. **Schedule a command to run at a specific time:**
   ```bash
   echo "backup.sh" | at 2:00 PM
   ```
   This schedules the `backup.sh` script to run at 2:00 PM today.

2. **Schedule a command for a specific date and time:**
   ```bash
   echo "echo 'Hello, World!'" | at 2023-10-31 10:00
   ```
   This will execute the command on October 31, 2023, at 10:00 AM.

3. **Schedule a command to run in 5 minutes:**
   ```bash
   echo "cleanup.sh" | at now + 5 minutes
   ```
   This command will run `cleanup.sh` five minutes from now.

4. **List scheduled jobs:**
   ```bash
   at -l
   ```
   This will display all jobs that are currently scheduled for the user.

5. **Remove a scheduled job:**
   ```bash
   at -d 3
   ```
   This removes the job with ID 3 from the schedule.

## Tips
- Always check your scheduled jobs using `at -l` to avoid confusion.
- Use the `-m` option if you want to receive notifications upon job completion.
- When scheduling commands, ensure that the commands are executable and that you have the necessary permissions.
- Consider using absolute paths for scripts and commands to avoid issues with the environment when the job runs.