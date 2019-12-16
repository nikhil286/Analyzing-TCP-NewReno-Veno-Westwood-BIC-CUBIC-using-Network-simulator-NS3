# Analyzing-TCP-NewReno-Veno-Westwood-BIC-CUBIC-using-Network-simulator-NS3
Comparative analysis of TCP New Reno, Veno, Westwood, BIC and CUBIC

NOTE:-
Steps to be followed-
1) To implement TCP New Reno on ns3, copy the application.cc file in scratch folder of ns-3.30(or latest version). Go to the folder 
ns-3.30 and open terminal there. Type the following command to run-

                         ./waf --run scratch/tcp.cc
After it runs successfully, pcap files are generated along with plt and cwnd files.
To plot the graph, open terminal and type 
                          gnuplot tcp.plt
2) To implement TCP Veno, open the application.cc file in any file editor, which was earlier copied in scratch folder. On line 130, change ns3::TcpNewReno to ns3::TcpVeno and save the file.
Go to the folder ns-3.30 and open terminal here. Type command

                        ./waf - -run scratch/tcp.cc


3) To implement TCP Westwood, open the application.cc file in any file editor, which was earlier copied in scratch folder. On line 130, change ns3::TcpNewReno to ns3::TcpWestwood and save the file.
Go to the folder ns-3.30 and open terminal here. Type command

                        ./waf - -run scratch/tcp.cc


4) To implement TCP BIC, open the application.cc file in any file editor, which was earlier copied in scratch folder. On line 130, change ns3::TcpNewReno to ns3::TcpBIC and save the file.
Go to the folder ns-3.30 and open terminal here. Type command

                        ./waf - -run scratch/tcp.cc
                        
Since CUBIC is not included in ns3
5) To implement TCP CUBIC, copy the tcpcubic.cc and tcpcubic.h files in ns-3.30->src->internet->model folder. Then go to internet   folder->Wscript. Do the following changes-
Line 163-->Type ‘model/Tcp-cubic.cc’
Line 402-->Type ‘model/tcp-cubic.h’ and save the file.

Go to the folder ns-3.30 and open terminal there. Type command

                        ./waf - -run scratch/tcpcubic.cc
After it runs successfully, pcap files for CUBIC are generated along with plt and cwnd files.
To plot the graph, open terminal and type 
gnuplot tcpcubic.plt

