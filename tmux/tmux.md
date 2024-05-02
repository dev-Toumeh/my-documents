## To reattach to an existing tmux session, use the command:
    tmux attach -t session_name

## to  list all sessions
    tmux list-sessions

## to resize panel
    - <Strg-b> + <Alt-up-arrow> or <Alt-left-arrow> or <Alt-down-arrow>
    - To resize tmux panes, you'll first want to hit your prefix — ctrl + b by default — and then the colon key :
    What this does is brings up a prompt at the bottom of your screen.
    Now you'll want to type in resize-pane in the prompt, followed by a hyphen - and either D, U, L, R. 
