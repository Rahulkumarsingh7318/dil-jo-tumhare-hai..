# dil-jo-tumhare-hai..
import time
import sys

# --- Configuration ---
# The delay between each character print (0.05 seconds is a good typing speed)
CHAR_DELAY = 0.05 
# ---------------------

def type_out_lyric(text, char_delay):
    """
    Prints a string character by character with a small delay.
    """
    for char in text:
        sys.stdout.write(char)
        sys.stdout.flush() # Force the character to appear immediately
        time.sleep(char_delay)
    
    # After the line is finished, print a newline character
    print()


def dil_jo_tumhara_hai_typing():
    """
    Plays the lyrics of 'Dil Ka Jo Haal Hai' with time gaps 
    and a dramatic typing effect.
    """
    print("\n--- Starting 'Dil Jo Tumhara Hai' (Typing Effect) ---\n")
    
    # Each tuple is (time_delay_in_seconds, lyric_line)
    # NOTE: The delay now accounts for the time it takes to type the previous line.
    lyrics_data = [
        # (Pause BEFORE printing the line, Line to print)
        (0.5, "💝 Dil ka jo haal hai"),
        (1.5, "Woh tujhe kaise bayaan kare"),
        (1.2, "🫣  Keh de tujhe ya dil mein rakhe"),
        (1.8, "Bolo na kya kare"),
        
        # --- Chorus Start ---
        (1.0, "🩵  Dil jo tumhara hai"),
        (1.2, "Kaisa bechara hai"),
        (1.5, "🫠  Maane na besharam"),
        (1.3, "Bilkul khatara hai"),
        # --- Chorus End ---
        
        (1.9, "💕  Tu kare dil beqaraar"),
        (2.6, "Kyun karoon main tujhse pyarr..."),
    ]

    # Process the lyrics
    for delay, line in lyrics_data:
        # 1. Wait for the specified time
        time.sleep(delay)
        
        # 2. Print the line with the typing effect
        type_out_lyric(line, CHAR_DELAY)

    print("\n--- End of Snippet ---\n")

# Execute the main function
if __name__ == "__main__":
    dil_jo_tumhara_hai_typing()
