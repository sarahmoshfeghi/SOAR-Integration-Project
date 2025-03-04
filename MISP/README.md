site : https://github.com/MISP/misp-docker# Install misp playbook

site https://github.com/MISP/misp-playbooks/blob/main/documentation/MISP%20playbook%20technical%20documentation.md
# Install misp playbook
```
git clone https://github.com/MISP/misp-playbooks.git
cd misp-playbooks/
python3 -m venv misp_env  # Create a virtual environment
source misp_env/bin/activate  # Activate the virtual environment
pip install pymisp # Install pymisp inside the venv
pip install pymisp jupyterlab notebook
mkdir -r playbooks/vault
mkdir -r playbooks/config
cp config/misp-playbook-jupyter.py playbooks/config/misp-playbook-jupyter.py
cp /opt/Misp/misp-playbooks/config/misp-playbook-jupyter.py playbooks/config/misp-playbook-jupyter.py
cp /opt/Misp/misp-playbooks/config/misp-playbook-jupyter.py ./misp-playbook-jupyter.py
mkdir  -r playbooks/my-playbooks

cp /opt/Misp/misp-playbooks/playbooks/config/misp-playbook-jupyter.service /etc/systemd/system
cat /etc/systemd/system/misp-playbook-jupyter.service
useradd -m -s /bin/bash playbook

systemctl daemon-reload
systemctl enable misp-playbook-jupyter.service
systemctl start misp-playbook-jupyter.service
journalctl -u misp-playbook-jupyter
```
