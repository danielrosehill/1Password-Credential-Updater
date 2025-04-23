# Idea For 1 Password Local AI Credential Manager

This repository is a work in progress for an idea that I'm planning on trying out. 

1Password is a fantastic password manager. One slowdown, however, is that many users, including me, migrated to this from other password managers, and in some cases, URI associations didn't hold or we never created them in the first place. This happens!

To give a simple example, you might have a safe credential for Reddit in your password vault, but you don't have reddit.com as the URI association. In this case, the extension will not prompt you for auto-completion when you're on reddit.com. 

My idea is that it would be fairly easy to resolve a lot of these issues with an AI tool.

The manual solution to this is going through your password vault and individually adding the missing associations, as at the time I'm writing this, there isn't a default matching utility. 

This, however, is tedious and really time-consuming to do at scale if you have a few thousand credentials spread over a few vaults. 

The idea for this is to mitigate security concerns by using a local LLM. I'll be using probably LLM 3.2 with Ollama in order to interact with the API to identify, firstly, credentials that are missing a URI, that have no URI association. Then, if there is an obvious association, the tool will write that out as a URL field for the credential.