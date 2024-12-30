# Altdns - Subdomain discovery 
Altdns is a DNS recon tool that allows for discovering subdomains that conform to patterns. It takes in words that could be present in subdomains under a domain (such as test, dev, staging) and a list of subdomains you know.

# Installation
Python 2:

pip install py-altdns==1.0.0

Python 3:

pip3 install py-altdns==1.0.2

# Usage
## altdns -i subdomains.txt -o data_output -w words.txt -r -s results_output.txt

subdomains.txt contains the known subdomains for an organization
data_output is a file that will contain the massive list of altered and permuted subdomains

words.txt is your list of words that you'd like to permute your current subdomains with (i.e. admin, staging, dev, qa) - one word per line
-r command resolves each generated, permuted subdomain

-s command tells altdns where to save the results of the resolved permuted subdomains. results_output.txt will contain the final list of permuted subdomains found that are valid and have a DNS record.

-t command limits how many threads the resolver will use simultaneously

-d 1.2.3.4 overrides the system default DNS resolver and will use the specified IP address as the resolving server. Setting this to the authoritative DNS server of the target domain may increase resolution performance
