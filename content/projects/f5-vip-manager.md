---
title: "F5 VIP Manager API"
date: 2025-03-10
---

This project involves building a Django API combined with a Bash script and mTLS configuration to automate the creation and management of F5 VIPs.

Here’s the high-level code for the Django API to create a VIP on an F5 device:

```python
from django.http import JsonResponse
import subprocess

def create_vip(request):
    vip_name = request.POST.get('vip_name')
    vip_ip = request.POST.get('vip_ip')

    # Execute the Bash script to create the VIP
    result = subprocess.run(['./create_vip.sh', vip_name, vip_ip], capture_output=True, text=True)

    if result.returncode == 0:
        return JsonResponse({"status": "success", "message": result.stdout})
    else:
        return JsonResponse({"status": "error", "message": result.stderr})
```

This integration allows for full automation and secure creation of F5 VIPs.