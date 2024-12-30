# Altdns - Subdomain discovery 
A DNS recon tool included in this package makes it possible to find subdomains that follow patterns. Altdns accepts a list of subdomains that you are aware of, as well as phrases that might appear in subdomains under a domain (e.g., test, dev, staging).


# Installation
 sudo apt install altdns

# Usage
## altdns -i subdomains.txt -o data_output -w words.txt -r -s results_output.txt

usage: altdns [-h] -i INPUT -o OUTPUT [-w WORDLIST] [-r] [-n] [-e] [-d DNSSERVER] [-s SAVE] [-t THREADS]

options:
  -h, --help            show this help message and exit
  -i INPUT, --input INPUT
                        List of subdomains input
  -o OUTPUT, --output OUTPUT
                        Output location for altered subdomains
  -w WORDLIST, --wordlist WORDLIST
                        List of words to alter the subdomains with
  -r, --resolve         Resolve all altered subdomains
  -n, --add-number-suffix
                        Add number suffix to every domain (0-9)
  -e, --ignore-existing
                        Ignore existing domains in file
  -d DNSSERVER, --dnsserver DNSSERVER
                        IP address of resolver to use (overrides system default)
  -s SAVE, --save SAVE  File to save resolved altered subdomains to
  -t THREADS, --threads THREADS
                        Amount of threads to run simultaneously

