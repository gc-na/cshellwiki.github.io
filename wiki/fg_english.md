# [Linux] Bash fg Usage equivalent: Bring a background job to the foreground

## Overview
The `fg` command in Bash is used to bring a background job to the foreground. This allows you to interact with the job directly in the terminal, enabling you to manage it as if it were started in the foreground initially.

## Usage
The basic syntax of the `fg` command is as follows:

```bash
fg [job_spec]
```

Here, `job_spec` refers to the specific job you want to bring to the foreground. If no job specification is provided, `fg` will default to the most recently suspended job.

## Common Options
- **`%n`**: Refers to the job number, where `n` is the job ID. You can find job IDs by using the `jobs` command.
- **`%string`**: Refers to the job with a name that matches `string`. This is useful if you have multiple jobs running and want to specify one by name.

## Common Examples
1. **Bringing the most recent job to the foreground**:
   ```bash
   fg
   ```

2. **Bringing a specific job by job number**:
   ```bash
   fg %1
   ```

3. **Bringing a job to the foreground by its name**:
   ```bash
   fg %my_script.sh
   ```

4. **If you have multiple jobs and want to see them**:
   ```bash
   jobs
   ```

5. **Bringing the second job in the list to the foreground**:
   ```bash
   fg %2
   ```

## Tips
- Use the `jobs` command to list all background jobs and their corresponding job IDs before using `fg`.
- If you have multiple jobs running, remember to specify the job you want to bring to the foreground to avoid confusion.
- If a job is stopped (suspended), you can resume it in the foreground using `fg` without needing to restart the job.