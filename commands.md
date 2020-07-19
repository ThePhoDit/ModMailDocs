---
description: This is the full list of available commands .
---

# Commands

{% hint style="info" %}
The prefix "/" is used in the examples. Please use yours.
{% endhint %}

### Reply to a message

```text
/reply {content}
```

**Aliases:** r  
**Thread Only:** true  
**Permission Level:** HELPER

### Close a thread

```text
/close
```

**Aliases:** c  
**Thread Only:** true  
**Permission Level:** HELPER

### Manage snippets \(predefined responses\)

```text
/snippet {add/delete} {name} {content}
```

**Aliases:** qr, quickreply  
**Thread Only:** false  
**Permission Level:** MANAGER

> To use snippets, just run the name as if it was a command.

### Manage the bot settings.

```text
/set {option} {value}
```

**Aliases:** s  
**Thread Only:** false  
**Permission Level:** MANAGER

| Option | Value |
| :--- | :--- |
| avatar | Image Link |
| username | Name |
| blacklist | {add/remove} {user ID} |

