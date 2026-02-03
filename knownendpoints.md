# Docs information

[x] General info about the company and why you should choose them by browsing to limestonenetworks.com

# Known GET API Endpoints

- [x] `https://api.dallas-idc.com/v2/facility/{LOCATION}/stock`
  - Known locations: DFW1, LAX1, SLC1, JFK1, DFW2, MIA1, ORD1, FRA1, PDX1, PAR1, TYO1, IAD1, LAX2, JFK2, TYO2, FRA2, SIN1, SLC2, AMS1, TYO1 Leased, ORD2, MIA2

- [x] `https://api.dallas-idc.com/v2/current_user`

- [ ] `https://api.dallas-idc.com/v2/sshkey`

- [ ] `https://api.dallas-idc.com/v2/image`

- [ ] `https://api.dallas-idc.com/v2/facility`

- [ ] `https://api.dallas-idc.com/v2/core`

- [ ] `https://api.dallas-idc.com/v2/project/{PROJECT_NAME}`

- [ ] `https://api.dallas-idc.com/v2/instance?project={PROJECT_NAME}`

- [ ] `https://api.dallas-idc.com/v2/job/{JOB_ID}` (Monitoring job status)

- [ ] `https://api.dallas-idc.com/v2/project?include_quotas=1&client_id={CLIENT_ID}`

# Known POST Endpoints

- [ ] `https://api.dallas-idc.com/v2/sshkey`
  - Example payload:
    ```json
    {
      "name": "zach@Zachs-MacBook-Pro.local",
      "pubkey": "ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIEnI9oIgTS7CEAFZXw5NDjGgx9icNSpLSpYC1LID6Yz4 zach@Zachs-MacBook-Pro.local"
    }
    ```

- [ ] `https://api.dallas-idc.com/v2/instance`
  - Example payload:
    ```json
    {
      "name": "test",
      "hostname": "bro.test.yo",
      "facility": "DFW1",
      "core": "bm1.e2234.1",
      "image": "almalinux-8",
      "keypair": "zach@Zachs-MacBook-Pro.local",
      "ssh_keys": ["zach@Zachs-MacBook-Pro.local"],
      "user_data": "#cloud-config\nhostname: demo-metal-node",
      "networks": ["public", "private"],
      "os_disk": "/dev/nvme0n1",
      "partitions": [],
      "admin_password": "hunter2isareallyBADpassword!",
      "tags": ["mytag"],
      "quantity": 1,
      "custom_metadata": {"user": "Zach"},
      "custom_image": "",
      "project_id": "PROJ-8ad55d52"
    }
    ```

# Auth Method

- Authorization: `Bearer {TOKEN}`
