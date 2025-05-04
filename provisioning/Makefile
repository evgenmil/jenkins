server:
	ansible-playbook -i hosts.yml server.yml

authorize:
	ansible-playbook -i hosts.yml authorize.yml

authorize-agent-key:
	ssh-keygen -q -t rsa -N '' -f files/agent_rsa

authorize-agents:
	ansible-playbook authorize-agents.yml -i hosts.yml

upgrade:
	ansible-playbook -i hosts.yml upgrade.yml

show-initial-password:
	ansible -b -i hosts.yml manager -m shell -a 'cd /home/deploy/jenkins && docker compose exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword'