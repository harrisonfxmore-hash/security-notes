# XSS Example

## Vulnerable Scenario
A simple web form that displays user input without sanitization:

<input type="text" name="comment">
<p id="display"></p>
<script>
  document.getElementById('display').innerHTML = document.querySelector('[name="comment"]').value;
</script>

## Attack Example
Input: <script>alert('XSS')</script>

## Impact
- Executes JavaScript in the user’s browser
- Can steal cookies, hijack accounts, or deface pages

## Mitigation
- Sanitize user input
- Use output encoding
- Implement Content Security Policy (CSP)
