# lab01C-
1.First, we create an instance of sf::TcpSocket  which allows us to connect to a remote socket

2.Then, we connect the socket. We convert the string 'address' to an sf::IpAddress ( instance by calling the constructor for sf::IpAddress. If the explicit constructor call is left out, it will be performed implicitly by the compiler anyway. After attempting a connection we check whether the connection succeeded by comparing the return value of the sf::TcpSocket::connect function  with the enumerator value sf::Socket::Done . If the two are equal, it means the connection succeeded and the port is open. In this case, the variable 'open' is set to true.

3.Next, we disconnect the socket using the sf::TcpSocket::disconnect function . This would be done automatically in the destructor if we left the explicit call out.

4.Finally, we return the value of 'open' to the calling function.

