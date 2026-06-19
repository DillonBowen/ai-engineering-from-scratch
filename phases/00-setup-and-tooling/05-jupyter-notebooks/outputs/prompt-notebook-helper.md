# Jupyter Notebook Helper

Common patterns and best practices for working in Jupyter notebooks.

## Magic Commands

| Command       | Type   | Purpose                              |
|---------------|--------|--------------------------------------|
| `%timeit`     | Line   | Time a single line (runs multiple times) |
| `%%timeit`    | Cell   | Time an entire cell (runs multiple times) |
| `%time`       | Line   | Time a single line (one run)         |
| `%%time`      | Cell   | Time an entire cell (one run)        |
| `%who`        | Line   | List all variables in namespace      |
| `%whos`       | Line   | Detailed list of variables           |
| `%reset`      | Line   | Clear all variables                  |
| `%matplotlib inline` | Line | Display plots inside the notebook |

## Cell Types

- **Code cells**: Run Python (or other kernels)
- **Markdown cells**: Write formatted text, headings, lists, code blocks
- **Raw cells**: Unprocessed content (rarely used)

## Best Practices

1. **One idea per cell** — makes debugging easier
2. **Use markdown cells** for explanations between code
3. **Restart & Run All** before sharing or submitting
4. **Clear outputs** before committing to git (or use `.gitignore`)
5. **Name variables clearly** — avoid `x`, `df`, `temp`

## Common Issues

- **Kernel died / Out of memory** → Reduce batch size or use smaller data
- **Plots not showing** → Make sure you used `%matplotlib inline`
- **Variables not updating** → Restart the kernel

## Useful Shortcuts

| Shortcut       | Action                     |
|----------------|----------------------------|
| `Shift + Enter` | Run cell and move to next  |
| `Ctrl + Enter`  | Run cell in place          |
| `A`             | Insert cell above          |
| `B`             | Insert cell below          |
| `M`             | Change cell to Markdown    |
| `Y`             | Change cell to Code        |
| `D, D`          | Delete cell                |