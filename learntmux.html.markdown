---
category: tool
tool: tmux
contributors:
    - ["kaernyk", "http://github.com/kaernyk"]
filename: LearnTmux.txt
---


  tmux is a terminal multiplexer: it enables a number of terminals to be
created, accessed, and controlled from a single screen. tmux may be detached
from a screen and continue running in the background, then later reattached.

  Once you feel comfortable manipulating tmux to suit your needs, I strongly 
suggest you read the man pages.



```
# Session Management
    
    tmux new         Create new session
    -s "Session"     Create named session
    -n "Window"      Create named Window
    -c "/dir"        Start in target directory

    C^b $            Rename current session
    C^b d            Detach current session
    C^b D            Select session to detach
    
    tmux attach      Attach last/available session
    -t "#"           Attach target session
    -d               Detach the session from other instances

    tmux ls          List open sessions
    C^b s            Select new session for attached client interactively
    
    kill-session     Kill current session
    -t "#"           Kill target session
    -a               Kill all sessions
    -a -t "#"        Kill all sessions but the target   


# Window Management

    C^b c            Create another window
    C^b "            Split Horizontally
    C^b %            Split Vertically
    C^b M-(1-5)      1) Tile vertically
                     2) Tile horizontally
                     3) Tile Vertically /w large horizontal
                     4) Tile horizontally /w large vertical 
                     5) Tile all windows evenly

    C^b q            Briefly display pane indexes
    C^#              Choose current window by #
    C^b w            Choose current window interactively
    C^b n            Change to next window
    C^b p            Change to previous window
    C^b Up, Right    Change to pane in selected direction 
        Down, left
    C^b {            Swap current/previous window
    C^b }            Swap current/next window

    C^b C-Up, Right  Resize in steps of one cell
         Down, left  
    C^b M-Up, Right  resize in steps of five cells
         Down, left  
    
    exit or C^b x    Kill the current window
```
