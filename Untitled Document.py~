def generate_concept_HTML(concept_title, concept_description):
    html_text_1 = '''
 <div class="concept">
    <div class="concept-title">
        ''' + concept_title
    html_text_2 = '''
    </div>
    <div class="concept-description">
        <p>
        ''' + concept_description
    html_text_3 = '''
    </p>
    </div>
 </div>'''
    
	full_html_text = html_text_1 + html_text_2 + html_text_3
    	return full_html_text





def make_HTML(concept):
    concept_title = concept[0]
    concept_description = concept[1]
    return generate_concept_HTML(concept_title, concept_description)

# This is an example of what a list of concepts might look like.
LIST_OF_CONCEPTS = [['Computer','A computer generally means a programmable machine. The two principal characteristics of a computer are: it responds to a specific set of instructions in a well-defined manner and it can execute a prerecorded list of instructions (a program).'],
                    [' Computer Program','A computer program is a list of instructions that tells the computer what to do. Some example of computer programs: A web broser like Firefox, Apple Safari can be used to view web pages on the internet.'],
                    [' Programming Language','A programming language is what programmers use to tell a computer what to do. There are many different languages for programming computers. Python is one of the programming language.'],
                    [' Python','Python is a programming language which is called an interpreter. That means it runs our programs, it inerprets them, excutes the programs that we wrote in Python language.'],
                    [' Grammar','Like English, programming languages also have a grammar that defines what strings are in the language.It is also useful in specifying how a parser should parse the language. Python language use a grammar notation called Backus-Naur-Form. The purpose of Backus-Naur-Form is to be able to precisely describe exactly the language in a way that is very simple and very concise.'],
                    [' Python Expressions','Expressions represent something, like a number or a string. Any value is an expression! If you type an expression on the command line, the interpreter evaluates it and displays the result: For example, print 1 + 1 is a valid expression but print 1 + will give error .When the Python shell displays the value of an expression, it uses the same format you would use to enter a value.']],
                    
def create_HTML_for_list_of_concepts(list_of_concepts):
    HTML = ""
    for concept in list_of_concepts:
        new_HTML = make_HTML(concept)
        HTML += new_HTML
    return HTML

print create_HTML_for_list_of_concepts(LIST_OF_CONCEPTS)
