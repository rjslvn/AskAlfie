### Unified Voice-Controlled Task Management

**Objective:** Create a code and mathematical framework for a voice-controlled AI assistant that manages complex multi-step tasks seamlessly.

**Code Framework:**

```python
class VoiceAssistant:
    def __init__(self):
        self.task_registry = {}  # Dictionary to map voice commands to task functions

    def add_task(self, command, task_function):
        """
        Register a voice command with its corresponding task function.
        
        Args:
            command (str): The voice command to register.
            task_function (function): The function to execute when the command is given.
        """
        self.task_registry[command] = task_function

    def execute_task(self, voice_command):
        """
        Execute a task based on a given voice command.
        
        Args:
            voice_command (str): The voice command to execute.
        """
        if voice_command in self.task_registry:
            task_function = self.task_registry[voice_command]
            task_function()
        else:
            print("Task not found.")

# Example tasks and commands
def schedule_appointment():
    print("Scheduling appointment...")

def order_groceries():
    print("Ordering groceries...")

# Example usage:
assistant = VoiceAssistant()
assistant.add_task("schedule appointment", schedule_appointment)
assistant.add_task("order groceries", order_groceries)

# Execute a task using voice command
assistant.execute_task("schedule appointment")
```

**Mathematical Framework:**

We can represent the voice-controlled task management as a mapping function `task_registry`, which maps voice commands (commands) to their corresponding task functions (task_function):

- `task_registry: command → task_function`

The `add_task` method registers a voice command with its associated task function, and the `execute_task` method executes a task based on a given voice command.

This framework allows the AI assistant to efficiently manage complex multi-step tasks through voice commands, ensuring that the appropriate task function is executed when a command is issued.

