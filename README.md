# gopacket-gtp
`gopacket` (v1.1.19) is not serializing GTP Extension Headers in the right way.
Extension Headers are appended to the buffer in multiple times instead of allocating the right size directly.
This results in a malformed packet since the extension ends up after the payload.

This fork indends to fix this.
