DCNM REST APIs calls for VXLAN EVPN Fabric automation
For any comments, please reach out to jucoutur@cisco.com

Disclaimer:
-----------
Work provided on an "AS IS" basis, without warranties or conditions of any kind. You are solely responsible for determining the appropriateness of using or redistributing this Work and assume any risks associated with your exercise of permissions under this License.

Before you start:
-----------------
Make sure you import the DCNM environment file, update the Postman vars with your own values and select the right env when running Postman.

Before creating any other call to DCNM, you need to log in using the 'Session - DCNM Login' call. This will save the token issued by DCNM and use it for any other subsequent calls (see Postman 'Tests' tab).


For creating a VRF/L3VNI:
-------------------------
  1. 'VRF - Create VRF'
  2. 'VRF - Attach VRF'
  3. 'VRF - Deploy VRF'

For deleting a VRF/L3VNI:
-------------------------
  1. 'VRF - Detach VRF'
  2. 'VRF - Deploy VRF'
  3. 'VRF - Delete VRF' (you nee to remove any Network attached to the VRF before removing it)


For creating a L2VNI:
---------------------
  1. 'Network - Create Network'
  2. 'Network - Attach Network'
  3. 'Network - Deploy Network'

For deleting a L2VNI:
---------------------
  1. 'Network - Detach Network'
  2. 'Network - Deploy Network'
  3. 'Network - Delete Network'

Misc:
-----
- 'Get list of existing networks/VRFs' will return an empty list '[]' along with 200 OK HTTP status when no network/VRF is present.
- You can use 'Fabric - Get Fabric inventory' to get the S/N of your switches (required in the environment to attach the config to a given node)
