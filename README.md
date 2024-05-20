
Overview
The Sphinx SUSI AI Theme is a theme designed specifically for Sphinx documentation, tailored to SUSI AI's projects. This theme provides a sleek and user-friendly interface for presenting technical documentation.

##
Features
- Custom HTML theme for Sphinx documentation.
- Integration with SUSI AI projects.
- Easy to install and configure.
- Customizable to fit project needs.

##
Installation Instructions
To install and set up the Sphinx SUSI AI Theme, follow the steps below:

1. Clone the repository:
    ```sh
    git clone https://github.com/loklak/sphinx_loklak_theme.git
    ```
2. Navigate to the cloned repository:
    ```sh
    cd sphinx_loklak_theme
    ```
3. Install the package using pip:
    ```sh
    pip install .
    ```

##
Usage Examples
To use the Sphinx SUSI AI Theme in your Sphinx project, add the following configuration to your `conf.py` file:

1. Import the theme:
    ```python
    import sphinx_susiai_theme
    ```
2. Set the theme in the configuration:
    ```python
    html_theme = 'sphinx_susiai_theme'
    html_theme_path = [sphinx_susiai_theme.get_html_theme_path()]
    ```

This will apply the SUSI AI theme to your Sphinx documentation.

##
Code Summary
The project structure comprises the following key files:

- **setup.py**: Contains the setup configuration for the package. It includes metadata such as the package name, version, author information, and the license. This file is essential for installing the theme.
    ```python
    from setuptools import setup

    setup(
        name='sphinx_susiai_theme',
        version='0.0.1',
        author='Balaji R',
        author_email='rbalajis25@gmail.com',
        url='https://github.com/fossasia/sphinx_susiai_theme',
        license='GNU',
        description='A Sphinx theme specific to SUSI AI\'s Projects',
        packages=['sphinx_susiai_theme'],
        include_package_data=True,
        entry_points={
            'sphinx.html_themes': [
                'sphinx_susiai_theme = sphinx_susiai_theme'
            ]
        }
    )
    ```

- **sphinx_susiai_theme/__init__.py**: Initializes the theme and provides functions necessary for Sphinx to locate and use it.
    ```python
    from os import path

    def setup(app):
        app.add_html_theme('sphinx_susiai_theme', path.abspath(path.dirname(__file__)))

    def get_html_theme_path():
        return path.abspath(path.dirname(path.dirname(__file__)))
    ```

##
Contributing Guidelines
We welcome contributions to improve the Sphinx SUSI AI Theme. To contribute:

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Make your changes.
4. Submit a pull request with a description of your changes.

Please make sure your code follows the existing coding style and includes tests where applicable.

##
License
This project is licensed under the [GNU General Public License](https://www.gnu.org/licenses/gpl-3.0.en.html).
```