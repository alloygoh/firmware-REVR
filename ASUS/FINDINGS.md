# Findings

# Main_AdmStatus_Content
There seems to be a hidden feature/page in the HTTP server, which on first look appears to allow for the activation of telnet service. The function can be found at 0x0003d744. The web page to trigger the function is `/Main_AdmStatus_Content.asp`. The `SystemCmd` param in the POST request get passed into `strncpy` and is eventually executed by a call to `system` .
