# aws-vpn-client-docker

> [!IMPORTANT]
> This repository is largely simply packaging other authors' work!
> 
> ## Credits
> 
> ### [samm-git/aws-vpn-client](https://github.com/samm-git/aws-vpn-client)
> 
> Alex Samorukov is the mastermind behind this implementation. He figured out how AWS patches the openvpn client and
> created the first implementations. Be sure to read his [blog](https://smallhacks.wordpress.com/2020/07/08/aws-client-vpn-internals/)
> on for more details.
> 
> ### [botify-labs/aws-vpn-client](https://github.com/botify-labs/aws-vpn-client)
> 
> Botify Labs maintains the `.patch` files for more recent versions of OpenVPN than what are available originally
> in Alex's repository.

---

This repository aims to package the work of Alex Samorukov and Botify Labs on making OpenVPN compatible with AWS VPN SAML.

## How to use

### Build the container yourself
1. Clone this repository
2. Download your AWS VPN client profile into a directory.
3. Adjust the mount source (`./profile.ovpn`) in `compose.yml` to read your ovpn profile file (`cvpn-endpoint-*.ovpn`)
   1. Don't change the mount target (`/opt/openvpn/profile.ovpn`)!
4. Run `docker compose up --build`
   1. Also grab the login link from `docker compose logs`
6. Enjoy

### Use a prebuilt container

_TODO_
