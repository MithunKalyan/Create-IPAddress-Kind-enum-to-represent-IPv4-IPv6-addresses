# EX-05: Create-IPAddress-Kind-enum-to-represent-IPv4-IPv6-addresses and create IP Address structure with IP Address Kind as a member and use this structure in the application.
# Aim:

To create an enum IPAddressKind in Rust that represents IPv4 and IPv6 addresses, define a struct IPAddress with IPAddressKind as a member, and use it in a Rust application.

# Algorithm:

1)Define an enum IPAddressKind with variants IPv4 and IPv6.

2)Define a struct IPAddress with:

    A field kind: IPAddressKind

    A field address: String

3)Implement a method display to print details of the IP address.

4)In the main function:

    Create IPv4 and IPv6 instances.

    Call display on them.

# Program:
```
Name:
Reg No:

enum IpAddrKind {
    V4,
    V6,
}

struct IpAddr {
    kind: IpAddrKind,
    address: String,
}

fn main() {

    let home = IpAddr {
        kind: IpAddrKind::V4,
        address: String::from("127.0.0.1"),
    };

    let loopback = IpAddr {
        kind: IpAddrKind::V6,
        address: String::from("::1"),
    };

    print_ip(&home);
    print_ip(&loopback);
}

fn print_ip(ip: &IpAddr) {
    match ip.kind {
        IpAddrKind::V4 => println!("IPv4 address: {}", ip.address),
        IpAddrKind::V6 => println!("IPv6 address: {}", ip.address),
    }
}
```

# Output:

# Result:

Thus, the program to create an enum for IPAddressKind, a struct for IPAddress, and demonstrated how to represent and print both IPv4 and IPv6 addresses in Rust is executed succesfully.
