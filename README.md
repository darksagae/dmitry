# dmitry
`Dmitry` (Deepmagic Information Gathering Tool) is a powerful tool for network reconnaissance included in Kali Linux. It is used for gathering information about a target domain, such as DNS information, email addresses, and open ports. Here's how to use it, along with examples and expected outputs.

### Installation

If `Dmitry` is not already installed on your Kali Linux system, you can install it using:

```bash
sudo apt-get install dmitry
```

### Basic Usage

The basic syntax for using `Dmitry` is:

```bash
dmitry [options] <target>
```

### Common Commands and Examples

1. **Basic Domain Information Gathering**:
   To gather basic information about a domain, use:

   ```bash
   dmitry -i example.com
   ```

   **Expected Output**:
   ```
   [*] DNS information for example.com
   [*] IP Address: 192.0.2.1
   [*] Name Servers: ns1.example.com, ns2.example.com
   ```

2. **Scanning for Open Ports**:
   To scan for open ports on a target, use the `-p` option:

   ```bash
   dmitry -p example.com
   ```

   **Expected Output**:
   ```
   [*] Open Ports for example.com
   [*] 22/tcp (SSH)
   [*] 80/tcp (HTTP)
   [*] 443/tcp (HTTPS)
   ```

3. **Email Enumeration**:
   To look for email addresses associated with a domain, use the `-e` option:

   ```bash
   dmitry -e example.com
   ```

   **Expected Output**:
   ```
   [*] Email addresses found for example.com
   [*] info@example.com
   [*] support@example.com
   ```

4. **Performing a Full Scan**:
   To perform a comprehensive scan that includes all available options, use:

   ```bash
   dmitry -winsepo example.com
   ```

   **Expected Output**:
   ```
   [*] DNS information for example.com
   [*] IP Address: 192.0.2.1
   [*] Open Ports: 22, 80, 443
   [*] Emails: info@example.com, support@example.com
   ```

### Conclusion

`Dmitry` is a versatile tool for gathering a wide range of information about a target domain. By using its various options, you can customize your reconnaissance efforts to gather valuable data for security assessments and penetration testing.




                                    ALTERNAIVE
`Dmitry` (Deepmagic Information Gathering Tool) is a command-line tool in Kali Linux used for gathering information about a host. It can collect various details, such as WHOIS information, TCP port scans, OS fingerprinting, and more.

### Installation

`Dmitry` is usually pre-installed on Kali Linux. If not, you can install it using:

```bash
sudo apt-get install dmitry
```

### Basic Usage

The basic syntax for using `dmitry` is:

```bash
dmitry [options] <target>
```

Here, `<target>` is the domain name or IP address you want to investigate.

### Common Options and Examples

1.  **WHOIS Information:**

    *   To retrieve WHOIS information, use the `-w` option:

    ```bash
    dmitry -w example.com
    ```

    *   **Expected Output:**

    ```
    -----WHOIS Information-----
    (output will vary depending on the domain)
    Registrar: ...
    Created: ...
    Updated: ...
    ```
2.  **TCP Port Scan:**

    *   To perform a TCP port scan, use the `-p` option:

    ```bash
    dmitry -p example.com
    ```

    *   **Expected Output:**

    ```
    -----TCP Scan Results-----
    (output will vary depending on open ports)
    Port 80: OPEN
    Port 443: OPEN
    ```
3.  **Subdomain Search:**

    *   To search for possible subdomains, use the `-s` option:

    ```bash
    dmitry -s example.com
    ```

    *   **Expected Output:**

    ```
    -----Subdomain Scan Results-----
    (output will vary depending on found subdomains)
    www.example.com
    mail.example.com
    ```
4.  **OS Fingerprinting:**

    *   To attempt OS fingerprinting, use the `-o` option:

    ```bash
    dmitry -o example.com
    ```

    *   **Expected Output:**

    ```
    -----Operating System Scan Results-----
    (output will vary depending on the OS and accuracy)
    Possible OS: Linux
    ```
5.  **Saving Results to a File:**

    *   To save the output to a text file, use the `-o` option followed by the filename:

    ```bash
    dmitry -w -p -s -o results.txt example.com
    ```

    This command will save WHOIS, port scan, and subdomain search results to `results.txt`.

### Important Notes

*   `Dmitry` can be noisy and may trigger intrusion detection systems.
*   The accuracy of OS fingerprinting can vary.
*   Always ensure you have permission to scan a target.

By combining these options, you can tailor `dmitry` to gather specific information, making it a useful tool for initial reconnaissance.




                                   ALTERNATIVE
Dmitry is a powerful tool in Kali Linux used for gathering information about a target system or network. It's a multi-function tool that can perform various tasks, including DNS lookups, whois queries, subnet calculations, and more.

Here's how to use Dmitri, along with examples and expected output:

**Installation**

Dmitry is typically pre-installed in Kali Linux. If not, you can install it using:

```
sudo apt-get install dmitry
```

**Basic Usage**

The basic syntax for using Dmitri is:

```
dmitry -o <output file> <target>
```

Where `<target>` is the domain name, IP address, or network range you want to scan.

**Common Options**

- `-o` or `--output`: Specify the output file for the scan results.
- `-d` or `--deep`: Perform a deep scan, which includes more detailed information.
- `-w` or `--whois`: Perform a whois query on the target.
- `-n` or `--net`: Perform a subnet calculation on the target.

**Examples**

1. **Basic Scan**:

```
dmitry -o output.txt example.com
```

This command will scan the `example.com` domain and gather information about the domain, including DNS records, whois information, and subnet calculations.

**Expected Output**:
```
[+] DNS Records:
  - example.com. IN A 192.0.2.1
  - example.com. IN MX mail.example.com
[+] Whois Information:
  - Domain Name: example.com
  - Registrant: Example Inc.
  - Registration Date: 2020-01-01
[+] Subnet Calculation:
  - Subnet: 192.0.2.0/24
  - Broadcast Address: 192.0.2.255
```

2. **Deep Scan**:

```
dmitry -o output.txt -d example.com
```

This command will perform a deep scan on the `example.com` domain, which includes more detailed information about the domain, including DNS records, whois information, subnet calculations, and more.

**Expected Output**:
```
[+] DNS Records:
  - example.com. IN A 192.0.2.1
  - example.com. IN MX mail.example.com
  - example.com. IN TXT "v=spf1 a mx ip4:192.0.2.1"
[+] Whois Information:
  - Domain Name: example.com
  - Registrant: Example Inc.
  - Registration Date: 2020-01-01
  - Expiration Date: 2025-01-01
[+] Subnet Calculation:
  - Subnet: 192.0.2.0/24
  - Broadcast Address: 192.0.2.255
  - Subnet Mask: 255.255.255.0
```

3. **Whois Query**:

```
dmitry -o output.txt -w example.com
```

This command will perform a whois query on the `example.com` domain.

**Expected Output**:
```
[+] Whois Information:
  - Domain Name: example.com
  - Registrant: Example Inc.
  - Registration Date: 2020-01-01
  - Expiration Date: 2025-01-01
```

These are just a few examples of how to use Dmitri. The tool offers many more options and features to help you gather information about target systems and networks.




                                       ALTERNATIVE
Understood. Here's how the `dmitry` tool in Kali Linux can be used, along with examples and expected output:

`Dmitry` (Deepmagic Information Gathering Tool) is a command-line tool used for gathering information about a target domain or IP address. It can be used to gather various types of information, such as subdomains, email addresses, and open ports.

**Installation**

`Dmitry` is typically pre-installed in Kali Linux. If it's not installed, you can install it using the following command:

```
sudo apt-get install dmitry
```

**Basic Usage**

The basic syntax for using `Dmitry` is:

```
dmitry [options] <target>
```

Where `<target>` is the domain name or IP address you want to gather information about.

**Common Options**

- `-w`: Perform a whois lookup on the target.
- `-s`: Scan the target for open ports.
- `-e`: Gather email addresses associated with the target.
- `-i`: Perform a reverse IP lookup on the target.
- `-p`: Perform a Google search for the target.

**Examples**

1. **Whois Lookup**:
   To perform a whois lookup on a target domain:

   ```
   dmitry -w example.com
   ```

   **Expected Output**:
   ```
   Performing whois lookup on example.com...
   
   [Whois data for example.com]
   ...
   ```

2. **Port Scan**:
   To scan a target for open ports:

   ```
   dmitry -s 192.168.1.100
   ```

   **Expected Output**:
   ```
   Performing port scan on 192.168.1.100...
   
   Open ports:
   - 22/tcp (ssh)
   - 80/tcp (http)
   - 443/tcp (https)
   ```

3. **Email Address Gathering**:
   To gather email addresses associated with a target domain:

   ```
   dmitry -e example.com
   ```

   **Expected Output**:
   ```
   Gathering email addresses for example.com...
   
   Email addresses found:
   - info@example.com
   - admin@example.com
   - support@example.com
   ```

4. **Reverse IP Lookup**:
   To perform a reverse IP lookup on a target:

   ```
   dmitry -i 192.168.1.100
   ```

   **Expected Output**:
   ```
   Performing reverse IP lookup on 192.168.1.100...
   
   Domains found:
   - example.com
   - subdomain.example.com
   ```

5. **Google Search**:
   To perform a Google search for a target:

   ```
   dmitry -p example.com
   ```

   **Expected Output**:
   ```
   Performing Google search for example.com...
   
   Google search results:
   - https://www.example.com
   - https://www.example.org
   - https://blog.example.com
   ```

`Dmitry` is a versatile tool that can help you gather a wide range of information about a target, which can be useful for reconnaissance and security assessments.




                                       ALTERNATIVE
`Dmitry` (Deepmagic Information Gathering Tool) is a powerful tool used for gathering information about a target. It is particularly useful for network reconnaissance and can help in penetration testing. Here’s how to use it, along with examples and expected outputs.

### Installation

If `Dmitry` is not already installed on your Kali Linux system, you can install it using:

```bash
sudo apt-get install dmitry
```

### Basic Usage

The basic syntax for using `Dmitry` is:

```bash
dmitry [options] <target>
```

### Common Options

- `-i`: Perform a DNS lookup.
- `-w`: Perform a WHOIS lookup.
- `-s`: Scan for open ports.
- `-e`: Gather email addresses associated with the domain.
- `-o`: Save output to a specified file.

### Examples

1. **Basic Information Gathering**:
   To gather basic information about a domain:

   ```bash
   dmitry -i -w example.com
   ```

   **Expected Output**:
   ```
   [*] Domain: example.com
   [*] IP Address: 192.0.2.1
   [*] WHOIS Info:
   ...
   ```

2. **Port Scanning**:
   To scan for open ports on a target:

   ```bash
   dmitry -s example.com
   ```

   **Expected Output**:
   ```
   [*] Scanning ports for example.com
   [*] Open Ports:
   22/tcp (SSH)
   80/tcp (HTTP)
   443/tcp (HTTPS)
   ```

3. **Email Address Gathering**:
   To find email addresses associated with a domain:

   ```bash
   dmitry -e example.com
   ```

   **Expected Output**:
   ```
   [*] Email Addresses found:
   info@example.com
   support@example.com
   ```

4. **Output to File**:
   To save the results to a file:

   ```bash
   dmitry -i -w example.com -o output.txt
   ```

   This command will create a file named `output.txt` with the gathered information.

### Conclusion

`Dmitry` is a versatile tool for information gathering, making it essential for reconnaissance during penetration testing. By utilizing various options, you can customize your data collection to suit your needs.




                                       ALTERNATIVE
`Dmitry` (Deepmagic Information Gathering Tool) is a command-line utility included in Kali Linux that is designed for gathering information about a target host. It can perform various tasks such as domain whois lookups, IP whois lookups, subdomain searches, email address searches, and TCP port scans.

### How to Use Dmitry

The basic syntax for using `Dmitry` is:

```bash
dmitry [options] <target>
```

### Common Options

- `-w`: Perform a whois lookup on the domain name.
- `-i`: Perform a whois lookup on the IP address.
- `-n`: Retrieve Netcraft information about the host.
- `-s`: Search for possible subdomains.
- `-e`: Search for possible email addresses.
- `-p`: Perform a TCP port scan.
- `-o <file>`: Save the output to a specified file.

### Examples

1. **Domain Whois Lookup**:
   To perform a whois lookup on a domain, you can use:

   ```bash
   dmitry -w example.com
   ```

   **Expected Output**:
   ```
   HostName: example.com
   HostIP: 93.184.216.119
   Whois information for example.com:
   - Registrar: Example Registrar
   - Creation Date: 2000-01-01
   ```

2. **IP Whois Lookup**:
   To perform a whois lookup on an IP address, use:

   ```bash
   dmitry -i 93.184.216.119
   ```

   **Expected Output**:
   ```
   HostIP: 93.184.216.119
   Whois information for 93.184.216.119:
   - Organization: Example Organization
   - Country: US
   ```

3. **Subdomain Search**:
   To search for subdomains of a domain, you can run:

   ```bash
   dmitry -s example.com
   ```

   **Expected Output**:
   ```
   Found subdomains:
   - www.example.com
   - api.example.com
   - mail.example.com
   ```

4. **TCP Port Scan**:
   To perform a TCP port scan on a host, use:

   ```bash
   dmitry -p example.com
   ```

   **Expected Output**:
   ```
   Open Ports:
   - 80/tcp (HTTP)
   - 443/tcp (HTTPS)
   ```

5. **Saving Output to a File**:
   To save the output of a command to a file, you can use the `-o` option:

   ```bash
   dmitry -winsepo output.txt example.com
   ```

   This command will save the results of the whois lookup, Netcraft information, subdomain search, email search, and TCP port scan to `output.txt`.

### Conclusion

`Dmitry` is a versatile tool for gathering information about domains and hosts. It can be particularly useful for penetration testing and security assessments, allowing users to collect valuable data about their targets.

---
Learn more:
1. [dmitry | Kali Linux Tools](https://www.kali.org/tools/dmitry/)
2. [How to use Dmitry to Scan Web Pages | by Scott Cosentino | Medium](https://scottc130.medium.com/how-to-use-dmitry-to-scan-web-pages-6adef108e80c)
3. [Dmitry - Passive Information Gathering Tool in Kali Linux - GeeksforGeeks](https://www.geeksforgeeks.org/dmitry-passive-information-gathering-tool-in-kali-linux/)
                              
