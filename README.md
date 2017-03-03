# GoBackN-Protocol

Go Back n is a connection oriented protocol in which the transmitter has a window of sequence numbers that may be transmitted without acknowledgment implemented in python.

The receiver will only accept the next sequence number it is expecting - other sequence nubmers are silently ignored.

The protocol has a maximum number of messages that can be sent without acknowledgement. If this window becomes full, the protocol is blocked until an acknowledgement is received for the earliest outstanding message. At this point the transmitter is clear to send more messages.
