def generate_concept_HTML(concept_title, concept_description):
    html_text_1 = '''
 <div class = "concept">
    <div class = "concept-title">        
        ''' + concept_title
    html_text_2 = '''
    </div>
      <div class = "concept-description">
          <p>
        ''' + concept_description
    html_text_3 = '''
          </p>
      </div>
  </div>
  '''
    
    full_html_text = html_text_1 + html_text_2 + html_text_3
    return full_html_text

def get_title(concept):
    start_location = concept.find('TITLE:')
    end_location = concept.find('DESCRIPTION:')
    title = concept[start_location + len('TITLE:'): end_location - 1]
    return title

def get_description(concept):
    start_location = concept.find('DESCRIPTION:')
    description = concept[start_location + len('DESCRIPTION:'):]
    return description

def get_concept_by_number(text, concept_number):
    counter = 0
    while counter < concept_number:
        counter = counter + 1
        next_concept_start = text.find('TITLE:')
        next_concept_end   = text.find('TITLE:', next_concept_start + 1)
        if next_concept_end >= 0:
            concept = text[next_concept_start:next_concept_end]
        else:
            next_concept_end = len(text)
            concept = text[next_concept_start:]
        text = text[next_concept_end:]
    return concept

TEST_TEXT = """
TITLE: Computer
DESCRIPTION: A computer generally means a programmable machine. The two principal characteristics of a computer are: it responds to a specific set of instructions in a well-defined manner and it can execute a prerecorded list of instructions (a program).

TITLE: Computer Program
DESCRIPTION:A computer program is a list of instructions that tells the computer what to do. Some example of computer programs: A web broser like Firefox, Apple Safari can be used to view web pages on the internet.

TITLE: Programming Language
DESCRIPTION: A programming language is what programmers use to tell a computer what to do. There are many different languages for programming computers. Python is one of the programming language.

TITLE: Python
DESCRIPTION: Python is a programming language which is called an interpreter. That means it runs our programs, it inerprets them, excutes the programs that we wrote in Python language.

TITLE: Grammar
DESCRIPTION: Like English, programming languages also have a grammar that defines what strings are in the language.It is also useful in specifying how a parser should parse the language. Python language use a grammar notation called Backus-Naur-Form. The purpose of Backus-Naur-Form is to be able to precisely describe exactly the language in a way that is very simple and very concise.

TITLE: Python Expressions
DESCRIPTION: Expressions represent something, like a number or a string. Any value is an expression! If you type an expression on the command line, the interpreter evaluates it and displays the result: For example, print 1 + 1 is a valid expression but print 1 + will give error .When the Python shell displays the value of an expression, it uses the same format you would use to enter a value. """






def generate_all_html(text):
    current_concept_number = 1
    concept = get_concept_by_number(text, current_concept_number)
    all_html = ''
    while concept != '':
        title = get_title(concept)
        description = get_description(concept)
        concept_html = generate_concept_HTML(title, description)
        all_html = all_html + concept_html
        current_concept_number = current_concept_number + 1
        concept = get_concept_by_number(text, current_concept_number)
    return all_html


print generate_all_html(TEST_TEXT)
