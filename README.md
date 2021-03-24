# Simple Mapi Client

This projects aim is to allow you to send emails with attachments via the default email client on windows. This currently relys upon windows MAPI32.dll, which is not recommended by Microsoft,
but there is currently no other way to do this from .NET.

This was not written by us here at Digital Anvil but was only dropped into a stand alone project so we could use it where we needed. We did have to 
tweak a couple things, but there's certainly no way we can take credit for the code.

The original source came from here: https://www.codeproject.com/Articles/17561/Programmatically-adding-attachments-to-emails-in-C

Sample usage in VB:
```
Dim ma As New DASimpleMAPI.MAPI
ma.AddRecipientTo("email@email.org")
ma.AddRecipientCC("email@emailtwo.org")
ma.AddAttachment(filename)
ma.SendMailPopup("this is a subject", "this is the body")
```
