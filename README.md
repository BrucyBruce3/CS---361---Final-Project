# CS-361
# Bruce Curtis
# Pseudo Random Prime Number Generator

Project Description:

This project is a Pseudo Random Prime Number Generator that finds a random number between 1 and 100,000 and finds the prime number less than or equal to that number.

It uses a micro service made by my partner Jeremy Talbert that includes the randomized number, which is stored in my comm_pipe.txt file and the new random prime number is stored in my num_request.txt file. The microservice file is called microservice.py.

The Microservice works between with my partner's main Mad Libs program. The Microservice takes the number of the mad lib story given by the user (which is written into the comm_pipe.txt file) and then populates the mad lib story into the story.txt file. This story and number of mad lib words to be replaced is then received by the main Mad Libs program.

Note: This Final Project adheres to the following communication contract:

Communication Contract:

A. The data is requested from the Microservice by reading the value of the selected story (for example "2") which is stored in the comm_pipe.txt file.

  Here is an example of a call (in Python):

        read_in = open("comm_pipe.txt", "r")
        read_line = read_in.readline()
        read_in.close()

B. The data is received from the Microservice by writing the story that corresponds to the value of the selected story.

  Here is an example of that process for the value of "2" (in Python):
        if read_line == "2":
            write_mad2 = open("story.txt", "w")
            print(f"Serving the story: 2")
            mad2 = "Pyramids~6~Pyramids are [adjective] tombs where Egyptians [past tense verb] their\n" \
                   "kings and [adjective] families. Some of them are [whole number] years old, each\n" \
                   "taking many [plural noun] to build. Each pyramid had [plural noun]  inside and\n" \
                   "were decorated with [plural noun]."
            write_mad2.write(mad2)
            write_mad2.close()


C. 
Please see the example of the UML Sequence Diagram below:

![image](https://user-images.githubusercontent.com/122341404/218589250-355685de-9dc5-46dc-8d49-1cecfdab945f.png)


