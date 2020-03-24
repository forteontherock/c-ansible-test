# USAGE

/usr/bin/ansible-playbook -vvv -i "localhost," -c local c-ansible-test/common.yml -e aws_region=$(curl -s http://169.254.169.254/latest/meta-data/placement/availability-zone | sed -e 's/.$//g') -e awslogs=enable -e "sshd=enable" > ~/kekka.txt
