## Task 1: Calculator Plus
**1) Create the repository on GitHub:**
- Repository name: 'git_assignment_HeroVired'
- Initialize with a README file.

**2) Clone the repository on your local machine:** 

`git clone` https://github.com/saimmoulvi/git_assignment_HeroVired.git

`cd git_assignment_HeroVired`

**3) Create and switch to the 'dev' branch:**

`git checkout -b dev`

**4) Add the initial Code:**

*Create a file named 'calculator.py' and add the following code:*

    import math

    class Calculator:
    
      def add(self, a, b):
        return a + b

      def subtract(self, a, b):
        return a - b

      def multiply(self, a, b):
        return a * b

      def divide(self, a, b):
        return a / b

    # TODO: Implement the following function to calculate the square root of a number.
      #def square_root(self, x):
          #return math.sqrt(x)

    if __name__ == "__main__":
     calculator = Calculator()

    num1 = 16
    num2 = 4

    print(f"{num1} + {num2} = {calculator.add(num1, num2)}")
    print(f"{num1} - {num2} = {calculator.subtract(num1, num2)}")
    print(f"{num1} * {num2} = {calculator.multiply(num1, num2)}")
    print(f"{num1} / {num2} = {calculator.divide(num1, num2)}")

    # TODO: Uncomment and test the square root feature.
    #num3 = 25
    #print(f"The square root of {num3} = {calculator.square_root(num3)}")

**5) Commit and push the changes**    

 `git add calculator.py`
 
 `git commit -m "Initial commit with basic arithmetic operations`
 
 `git push -u origin dev`

 **6) Merge 'dev' branch into 'main' branch**

 `git checkout main`

 `git merge dev`

 `git push origin main`

 **7) Create a release on Github:**
- Go to the repository on GitHub.
- Click on Releases" -> "Draft a new release".
- Tag version 'v1.0'
- Release title: 'CalculatorPlus v1.0'
- Description: Initial release with basic arithmetic operations.
- Publish the release.

**8) Add a collaborator:**
- Go to the repository on Github
- Click on "Settings" -> "Collaborators" -> "Add collaborator"
- Enter your classmate's GitHub Username and add them.

**9) Create and switch to the 'feature/sqrt' branch**

  `git checkout -b feature/sqrt`

**10) Implement the 'sqrt' feature in 'calculator.py':**  

    import math

    class Calculator:
    
      def add(self, a, b):
        return a + b

      def subtract(self, a, b):
        return a - b

      def multiply(self, a, b):
        return a * b

      def divide(self, a, b):
        return a / b

    # TODO: Implement the following function to calculate the square root of a number.
      def square_root(self, x):
          return math.sqrt(x)

    if __name__ == "__main__":
     calculator = Calculator()

    num1 = 16
    num2 = 4

    print(f"{num1} + {num2} = {calculator.add(num1, num2)}")
    print(f"{num1} - {num2} = {calculator.subtract(num1, num2)}")
    print(f"{num1} * {num2} = {calculator.multiply(num1, num2)}")
    print(f"{num1} / {num2} = {calculator.divide(num1, num2)}")

    # TODO: Uncomment and test the square root feature.
    num3 = 25
    print(f"The square root of {num3} = {calculator.square_root(num3)}")

**11) Commit and push the changes:**

`git add calculator.py`

`git commit -m "Implemented square root feature"`

`git push -u origin feature/sqrt`

**12) Switch back to the 'dev' branch:**

`git checkout dev`

**13) Fix the bug in the 'divide' function:**

    def divide(self, a, b):
        if b == 0:
            raise ValueError("Cannot divide by zero.")
        return a / b
        
**14) Commit and push the changes:**

`git add calculator.py`

`git commit -m "Fixed divide function to handle division by zero"`

`git push origin dev`

**15) Keep the 'feature/sqrt' branch up-to-date:**

`git checkout feature/sqrt`

`git merge dev`

`git push origin feature/sqrt`

**16) Create a pull request on GitHub:**
- Go to the repository on Github
- Switch to the 'feature/sqrt' branch
- Click on "Pull request" -> "New Pull Request"
- Base: 'main' , Compare: 'feature/sqrt'
- Create the pull request.

**17) Request a code review:**
- Add your classmate or team member as a reviewer.
- Wait for the review and approval.

**18) After approval, merge the pull request:**
-Merge the 'feature/sqrt' pull request into the 'dev' branch.

**19) Test the 'dev' branch:**
- Ensure that all features work correctly in the 'dev' branch.

**20)Merge 'dev' branch into 'main' branch**

`git checkout main`

`git merge dev`

`git push origin main`

**21) Create a second release on GitHub:**
- Go to the repository on GitHub
- Click on "Releases" -> "Draft a new release".
- Tag Version: 'v2.0'
- Release title: 'CalculatorPlus v2.0'
- Description: Added squre root feature and fixed division by zero bug.
- Publish the release.

## Task 2: Large File Storage (lfs):

**1) First we need to install git lfs**
- Open the windows command prompt and run the below command
  
  `git lfs install`

**2) Initialize Git LFS in your existing 'git_assignment_HeroVired' repository**
- Open git bash and run the following command

  `cd git_assignment_HeroVired`

  `git lfs install`

**3) Create and switch to the lfs branch**

  `git checkout -b lfs`
  
**4) Track large file with Git LFS over 200MB**

  `git lfs  track "*.mkv"`

*We need to specify the file extension pattern that matches our large file.*

**5) Add a large binary file**

*Upload any type of file over 200MB. In our scenario we are adding a file named video.mkv*

**6) Add, Commit, and push the binary file**

 `git add .gitattributes large_file.bin`

 `git commit -m "Added large video file using LFS`

 `git push origin lfs`

### Verify the setup on another machine

**1) Clone the repository:**

 `git clone` https://github.com/saimmoulvi/git_assignment_HeroVired.git

 `cd git_assignment_HeroVired`

**2) Checkout the 'lfs' branch:**

 `git checkout lfs`

**3) Pull the LFS file:**

 `git lfs pull`

**4) Verify the video file is downloaded correctly** 

## Task 3: Calculating area of circle and square ##

**1) Create and switch to the 'feature/circle-area' branch:**

  `git checkout -b feature/circle-area`

**2) Add the circle area calculation code in 'geometry_calculator.py**

    import math

    class GeometryCalculator:
        def calculate_circle_area(self, radius):
            return math.pi * radius ** 2

    def calculate_rectangle_area(self, length, width):
        return length * width

    if __name__ == "__main__":
        calculator = GeometryCalculator()

    # TODO: Implement the feature to calculate the area of a circle
    radius = 5
    print(f"The area of the circle with radius {radius} = {calculator.calculate_circle_area(radius)}")

    # TODO: Implement the feature to calculate the area of a rectangle
    #length = 10
    #width = 6
    #print(f"The area of the rectangle with length {length} and width {width} = {calculator.calculate_rectangle_area(length, width)}")

**3) Stash changes for Circle Area Feature**

  `git stash`

**4) Verify if the working directory is clean or not**

  `git status`

**5) Create and switch to the 'feature/rectangle_area' branch:**

  `git checkout -b feature/rectangle-area`

**6) Add the rectangle area calculation code in 'geometry_calculator.py':**

    import math

    class GeometryCalculator:
        def calculate_circle_area(self, radius):
            return math.pi * radius ** 2

    def calculate_rectangle_area(self, length, width):
        return length * width

    if __name__ == "__main__":
        calculator = GeometryCalculator()

    # TODO: Implement the feature to calculate the area of a circle
    radius = 5
    print(f"The area of the circle with radius {radius} = {calculator.calculate_circle_area(radius)}")

    # TODO: Implement the feature to calculate the area of a rectangle
    length = 10
    width = 6
    print(f"The area of the rectangle with length {length} and width {width} = {calculator.calculate_rectangle_area(length, width)}")

**7) Stash the changes for Rectangle Area Feature**

  `git stash`

**8) Verify the working directory is clean:**

  `git status`

**9) Switch back to the 'feature/circle-area' branch:**

  `git checkout feature/circle-area`

**10) Retrieve the stashed changes:**

  `git stash pop`

**11) Complete the circle area feature implementation and save the changes:**

    import math

    class GeometryCalculator:
        def calculate_circle_area(self, radius):
            return math.pi * radius ** 2

    def calculate_rectangle_area(self, length, width):
        return length * width

    if __name__ == "__main__":
        calculator = GeometryCalculator()

    # TODO: Implement the feature to calculate the area of a circle
    radius = 5
    print(f"The area of the circle with radius {radius} = {calculator.calculate_circle_area(radius)}")

    # TODO: Implement the feature to calculate the area of a rectangle
    #length = 10
    #width = 6
    #print(f"The area of the rectangle with length {length} and width {width} = {calculator.calculate_rectangle_area(length, width)}")

**12) Commit and Push Circle Are Feature:**

  `git add geometry_calculator.py`

  `git commit -m "Feature/Area of Circle`

  `git push origin feature/circle-area`

**13) Switch back to the 'feature/rectangle-area' branch:**

  `git checkout feature/rectangle-area`

**14) Retrieve the stashed changes:**

  `git stash pop`

**15) Complete the rectangle area feature implementation and save the changes:**

    import math

    class GeometryCalculator:
        def calculate_circle_area(self, radius):
            return math.pi * radius ** 2

    def calculate_rectangle_area(self, length, width):
        return length * width

    if __name__ == "__main__":
        calculator = GeometryCalculator()

    # TODO: Implement the feature to calculate the area of a circle
    radius = 5
    print(f"The area of the circle with radius {radius} = {calculator.calculate_circle_area(radius)}")

    # TODO: Implement the feature to calculate the area of a rectangle
    length = 10
    width = 6
    print(f"The area of the rectangle with length {length} and width {width} = {calculator.calculate_rectangle_area(length, width)}")

**16) Commit and push Rectangle Area Feature:**

  `git add geometry_calculator.py`
  
  `git commit -m "Feature: Area of rectangle`
  
  `git push origin feature/rectangle-area`

**17) Create pull request on GitHub:**
- Go to the repository on GitHub
- Create a pull request for the 'feature/circle-area' branch targeting the dev branch.
- Create a pull request for the 'featture/rectangle-area' branch targeting the dev branch.

**18) Request for code review and approval**

**19) After receiving approval, merge both the pull requests into the 'dev' branch**
  








  
  

 





    


    

  
 









