# Valence Robotics' ElectroDNS

Open source DNS records for Valence Robotics powered by OctoDNS, Github Actions, and Cloudflare.

## Usage

This is for Valence Robotics team members only. This can be used to configure a subdomain for offical Valence Robotics projects. For example, `valencerobotics.com` is the main domain, and `docs.valencerobotics.com` is a subdomain. This repository is used to configure the DNS records for `docs.valencerobotics.com`.

## Adding a subdomain

This section was borrowed from Hack Club DNS. Thanks Hack Club!

1. [Create a fork](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/fork-a-repo) of this repository.
2. In your fork open the [valencerobotics.org.yaml](./valencerobotics.org.yaml) file and add the following alphabetically based off the subdomain name:

```yaml
SUBDOMAIN_NAME:
  - ttl: 1
    type: CNAME
    value: SOURCE_DOMAIN_OR_IP.
```

3. Replace `SUBDOMAIN_NAME` with the name of the sub-domain. So if the name was `hello` then the subdomain would be `hello.valencerobotics.org`.
4. Replace `SOURCE_DOMAIN_OR_IP` with the domain or IP address of the website you want the subdomain to go. If you are using an IP address change `type: CNAME` to `type: A`. Remember to leave that `.` at the end!
5. Commit your changes and [create the PR](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request-from-a-fork)!

That's it! Someone with contributor access to the repo will then review your PR.
