# [Linux] Bash jobs uso: Manage background jobs in the shell

## Overview
The `jobs` command in Bash is used to display the status of jobs that are running in the background or have been suspended in the current shell session. It provides information about the jobs, including their job numbers, statuses, and process IDs.

## Usage
The basic syntax of the `jobs` command is as follows:

```bash
jobs [options] [arguments]
```

## Common Options
- `-l`: Show process IDs along with job information.
- `-n`: Display only jobs that have changed status since the last time the command was run.
- `-p`: Show only the process IDs of the jobs.

## Common Examples

1. **List all background jobs:**
   To see all jobs running in the background, simply use:
   ```bash
   jobs
   ```

2. **List jobs with process IDs:**
   To include process IDs in the output, use the `-l` option:
   ```bash
   jobs -l
   ```

3. **Show only jobs that have changed status:**
   To display only jobs that have changed since the last check, use:
   ```bash
   jobs -n
   ```

4. **Display only process IDs of jobs:**
   If you want to see just the process IDs of the jobs, you can use:
   ```bash
   jobs -p
   ```

## Tips
- Use `bg` to resume a suspended job in the background after checking its status with `jobs`.
- Use `fg` to bring a background job to the foreground if you need to interact with it.
- Remember that the job numbers displayed by `jobs` can be used with `bg` and `fg` commands to manage jobs effectively. For example, `fg %1` brings job number 1 to the foreground.