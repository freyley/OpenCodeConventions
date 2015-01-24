Good exception handling catches errors and deals with them appropriately. Bad exception handling suppresses errors.

Don't do this:
try:
    do_a_thing()
except: pass

Do this:
try:
    do_a_thing()
except ThingException, te:
    log("Error attempting to do a thing, rerouting. Error was: {0}".format(te)
    fail_gracefully()

