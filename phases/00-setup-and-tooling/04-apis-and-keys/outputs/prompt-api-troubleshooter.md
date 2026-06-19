# Prompt & API Troubleshooter

Common API errors and how to fix them.

## 1. 401 Unauthorized
**Cause:** Missing or invalid API key  
**Fix:**
- Check that `ANTHROPIC_API_KEY` is set in your environment or `.env` file
- Make sure there are no extra spaces or quotes around the key
- Verify the key is active in the Anthropic console

## 2. 429 Too Many Requests (Rate Limit)
**Cause:** You exceeded the allowed requests per minute  
**Fix:**
- Wait and retry (usually 1 minute)
- Implement exponential backoff in code
- Check your usage limits in the dashboard

## 3. 400 Bad Request
**Cause:** Malformed request body (wrong model name, invalid JSON, etc.)  
**Fix:**
- Double-check the model name (`claude-3-5-sonnet-20241022`, etc.)
- Validate your JSON payload
- Check that `max_tokens` is set

## 4. 529 Overloaded
**Cause:** Anthropic servers are temporarily overloaded  
**Fix:**
- Wait a few seconds and retry
- Use a fallback model if available

## 5. No response / Timeout
**Cause:** Network issue or very large request  
**Fix:**
- Check your internet connection
- Reduce `max_tokens` or prompt length
- Add a timeout to your HTTP request

## Quick Checklist
- [ ] API key is set and correct
- [ ] Using the right model name for the date
- [ ] `max_tokens` is reasonable
- [ ] Request body is valid JSON
- [ ] Using the correct API version header

## Raw HTTP vs SDK
Use the raw HTTP version when you need to debug exactly what is being sent. The SDK hides many details that are useful for learning.