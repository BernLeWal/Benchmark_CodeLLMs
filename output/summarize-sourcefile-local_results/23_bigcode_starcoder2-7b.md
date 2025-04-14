<</EXERCISENAME>>


<</EXERCISENAME>>

<</EXERCISENAME>>


<</EXERCISENAME>>

e:
    def __init__(self, name):
        self.name = name

    def __str__(self):
        return str(self.name)


class Employee(Person):
    def __init__(self, name, salary):
        super().__init__(name)
        self.salary = salary

    def __str__(self):
        return str(self.name) + " " + str(self.salary)


class Student(Person):
    def __init__(self, name):
        super().__init__(name)
        self.grade = 0

    def __str__(self):
        return str(self.name) + " " + str(self.grade)


class School:
    def __init__(self, name):
        self.name = name

        # TODO: create an empty dictionary
        self.students = dict()
        self.employees = dict()

    def __str__(self):
        return self.name


class SchoolClass:
    def __init__(self, name, school):
        self.name = name
        self.school = school

        # TODO: create an empty dictionary
        self.students = dict()
        self.employees = dict()

    def __str__(self):
        return self.name


# TODO: implement a method to add a person to the school class
def addPerson(person, school):
    # TODO: implement a method to add a person to the school class
    # TODO: implement a method to add a person to the school class
    # TODO: implement a method to add a person to the school class
    # TODO: implement a method to add a person to the school class
    # TODO: implement a method to add a person to the school class


# TODO: implement a method to add a person to the school class
def addPersonInClass(person, schoolClass):
    # TODO: implement a method to add a person to the school class
    # TODO: implement a method to add a person to the school class
    # TODO: implement a method to add a person to the school class
    # TODO: implement a method to add a person to the school class


# TODO: implement a method to remove a person to the school class
def removePerson(person, school):
    # TODO: implement a method to remove a person to the school class
    # TODO: implement a method to remove a person to the school class
    # TODO: implement a method to remove a person to the school class
    # TODO: implement a method to remove a person to the school class


# TODO: implement a method to remove a person to the school class
def removePersonInClass(person, schoolClass):
    # TODO: implement a method to remove a person to the school class
    # TODO: implement a method to remove a person to the school class
    # TODO: implement a method to remove a person to the school class
    # TODO: implement a method to remove a person to the school class


# TODO: implement a method to get all students of a school
def getAllStudents(school):
    # TODO: implement a method to get all students of a school
    # TODO: implement a method to get all students of a school
    # TODO: implement a method to get all students of a school
    # TODO: implement a method to get all students of a school


# TODO: implement a method to get all employees of a school
def getAllEmployees(school):
    # TODO: implement a method to get all employees of a school
    # TODO: implement a method to get all employees of a school
    # TODO: implement a method to get all employees of a school
    # TODO: implement a method to get all employees of a school


# TODO: implement a method to get all students in a school class
def getAllStudentsInClass(schoolClass):
    # TODO: implement a method to get all students in a school class
    # TODO: implement a method to get all students in a school class
    # TODO: implement a method to get all students in a school class
    # TODO: implement a method to get all students in a school class


# TODO: implement a method to get all employees in a school class
def getAllEmployeesInClass(schoolClass):
    # TODO: implement a method to get all employees in a school class
    # TODO: implement a method to get all employees in a school class
    # TODO: implement a method to get all employees in a school class
    # TODO: implement a method to get all employees in a school class


# TODO: implement a method to get all persons in a school class
def getAllPersonsInClass(schoolClass):
    # TODO: implement