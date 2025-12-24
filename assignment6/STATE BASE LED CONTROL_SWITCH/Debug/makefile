################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (13.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := STATE BASE LED CONTROL_SWITCH
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
STATE\ BASE\ LED\ CONTROL_SWITCH.elf \

MAP_FILES += \
STATE\ BASE\ LED\ CONTROL_SWITCH.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
STATE\ BASE\ LED\ CONTROL_SWITCH.list \


# All Target
all: main-build

# Main-build Target
main-build: STATE\ BASE\ LED\ CONTROL_SWITCH.elf secondary-outputs

# Tool invocations
STATE\ BASE\ LED\ CONTROL_SWITCH.elf STATE\ BASE\ LED\ CONTROL_SWITCH.map: $(OBJS) $(USER_OBJS) D:\arm\ controller\Pranjal_94136\Pranjal_94136\assignment6\STATE\ BASE\ LED\ CONTROL_SWITCH\STM32F407VGTX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "STATE BASE LED CONTROL_SWITCH.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\arm controller\Pranjal_94136\Pranjal_94136\assignment6\STATE BASE LED CONTROL_SWITCH\STM32F407VGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="STATE BASE LED CONTROL_SWITCH.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

STATE\ BASE\ LED\ CONTROL_SWITCH.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "STATE BASE LED CONTROL_SWITCH.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) STATE\ BASE\ LED\ CONTROL_SWITCH.elf STATE\ BASE\ LED\ CONTROL_SWITCH.list STATE\ BASE\ LED\ CONTROL_SWITCH.map STATE\\ BASE\\ LED\\ CONTROL_SWITCH.elf default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
