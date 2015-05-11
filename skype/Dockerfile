
FROM base/archlinux 

RUN useradd --create-home user

RUN sed -i -e'/^#\[multilib\]/{s/#//;N;s/#//;N;s/#//}' /etc/pacman.conf

RUN pacman-key --lsign-key 753E0F1F && pacman-key -r 753E0F1F
RUN pacman --noconfirm -Sy skype

USER user
VOLUME /home/user
CMD ["skype"]
