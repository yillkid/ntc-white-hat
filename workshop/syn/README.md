## 使用 dcpdump
- 可以觀察出
  1. 隨機產生的 source IP
  2. 全部為 SYN flag
```bash=
# tcpdump -i lo port 9999
tcpdump: verbose output suppressed, use -v or -vv for full protocol decode
listening on lo, link-type EN10MB (Ethernet), capture size 262144 bytes
17:18:19.434935 IP 220-244-189-68.static.tpgi.com.au.7799 > localhost.9999: Flags [S], seq 0, win 8192, length 0
17:18:19.436923 IP 253.228.154.96.34984 > localhost.9999: Flags [S], seq 0, win 8192, length 0
17:18:19.439004 IP 157.72.18.161.5160 > localhost.9999: Flags [S], seq 0, win 8192, length 0
17:18:19.441238 IP 238.26.229.119.40551 > localhost.9999: Flags [S], seq 0, win 8192, length 0
17:18:19.442844 IP 71.27.195.19.34804 > localhost.9999: Flags [S], seq 0, win 8192, length 0
17:18:19.444045 IP 189-79-118-178.dsl.telesp.net.br.40302 > localhost.9999: Flags [S], seq 0, win 8192, length 0
17:18:19.445218 IP ip66-3-152-126.z152-3-66.customer.algx.net.34567 > localhost.9999: Flags [S], seq 0, win 8192, length 0
17:18:19.446335 IP ool-1859bc8e.static.optonline.net.42592 > localhost.9999: Flags [S], seq 0, win 8192, length 0
17:18:19.447449 IP 204.118.137.184.17211 > localhost.9999: Flags [S], seq 0, win 8192, length 0
17:18:19.448737 IP c-73-228-65-236.hsd1.ut.comcast.net.40964 > localhost.9999: Flags [S], seq 0, win 8192, length 0
17:18:19.449839 IP 71.220.137.57.bcube.co.uk.35601 > localhost.9999: Flags [S], seq 0, win 8192, length 0
17:18:19.450906 IP 173-17-203-203.client.mchsi.com.50789 > localhost.9999: Flags [S], seq 0, win 8192, length 0
17:18:19.451957 IP ip123-034.netfree.cz.54857 > localhost.9999: Flags [S], seq 0, win 8192, length 0
17:18:19.453069 IP 163.128.194.41.42 > localhost.9999: Flags [S], seq 0, win 8192, length 0
17:18:19.454168 IP 6.89.118.44.48710 > localhost.9999: Flags [S], seq 0, win 8192, length 0
17:18:19.455223 IP static.vnpt.vn.39497 > localhost.9999: Flags [S], seq 0, win 8192, length 0
17:18:19.762010 IP 50-103-1-251.dklb.il.frontiernet.net.45706 > localhost.9999: Flags [S], seq 0, win 8192, length 0
17:18:19.965334 IP 247.10.250.33.55340 > localhost.9999: Flags [S], seq 0, win 8192, length 0
```
