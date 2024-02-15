# -class Telephone:
    def __init__(self, number):
        self.number = number
        self.call_history = []

    def make_call(self, recipient):
        print(f"Calling {recipient}...")
        self.call_history.append({"type": "outgoing", "recipient": recipient})

    def receive_call(self, caller):
        print(f"Incoming call from {caller}...")
        self.call_history.append({"type": "incoming", "caller": caller})

    def view_call_history(self):
        print("Call History:")
        for call in self.call_history:
            if call["type"] == "outgoing":
                print(f"Outgoing call to {call['recipient']}")
            else:
                print(f"Incoming call from {call['caller']}")


# Example usage
if __name__ == "__main__":
    # Create a telephone instance
    my_phone = Telephone("123-456-7890")

    # Make a call
    my_phone.make_call("987-654-3210")

    # Receive a call
    my_phone.receive_call("555-555-5555")

    # View call history
    my_phone.view_call_history()
