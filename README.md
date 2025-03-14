Well, hello. You've made it to my secret hub of operations.
You may be one of the first. You got here by inspecting outgoing connections by Triage or Wireshark. You found it leads to a strange GET request from a GitHub page.
This is actually something pretty important. Here is my "control switch" for Vizzle Executor. If the status is false, execution or even injection are disabled forcing it into a de-facto disabled state.
If you hoped to find something malicious, well, I can promise to you there isn't anything malicious.

Usually, I wouldn't tell people how to bypass a kill switch dependent on a GitHub file, but here's how.
- Get some kind of Man-In-The-Middle HTTP proxy that can intercept the get request coming from Vizzle.
- Instead of allowing it to, for example, return "False", make it return True.
And if you restart Vizzle, execution should now be enabled!

However, I do have to say very strictly that this means any kind of losses or problems originating from you bypassing the kill switch (for example: forcing Vizzle to start executing even if the killswitch is off and I don't want people losing their accounts) will not be covered by my "responsibility". You knowingly bypassed a feature which I seek to defend my users with.
So, with all that said - you're on your own.
Good luck, dear person.
